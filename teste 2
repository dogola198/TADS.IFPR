Douglas

#include <stdio.h>
#include <stdlib.h>

struct no
{
    int info;
    struct no *next;
};

typedef struct no No;

void mostra(No*lst)
{
    No*p;
    for (p = lst; p != NULL; p = p -> next)
    {
        printf("%d -> ", p->info);
    }
    printf("NULL\n");
}


No *stacktop(No *lst)
{
    No * p;
    p = lst->next;
    return p->info;
}

void push(No *p, int y)
{
    No *nova;
    nova = malloc(sizeof(No));
    nova -> info = y;
    nova -> next = p -> next;
    p -> next = nova;
}

int pop (No *p)
{
    if (p -> next !=NULL)
    {
        int x;
        No *lixo;
        lixo = p -> next;
        p -> next = lixo -> next;
        x = lixo->info;
        printf("%d Removido.\n", x);
        free(lixo);
    }
    else if (p ->next == NULL)
        printf("Pilha vazia (underflow).\n");
}


int main()
{

    No c, lst;
    c.next = NULL;
    lst = c;

    int x = 0;

    int opcao = 0;
    printf("BEM VINDO AO INCRIVEL CRIADOR DE PILHAS!!\n1 para push\n2 para pop\n3 para stacktop\n4 para mostrar\n5 para limpar a tela\n6 para sair\n\n");
    scanf("%d", &opcao);

while (opcao != 6)
{
    if (opcao == 1)
    {
        printf("Insira o valor: ");
        scanf("%d\n", &x);
        push(&lst, x);
    }
    else if (opcao == 2)
    {
        pop(&lst);
    }

   else if (opcao == 3)
    {
        printf("Ultimo elemento da pilha: %d\n", stacktop(&lst));
    }
    else if (opcao == 4)
    {
        mostra(lst.next);
    }

    else if (opcao == 5)
    {
        system("clear");
        printf("\n1 para inserir\n2 para remover\n3 para busca\n4 para mostrar\n5 para limpar a tela\n6 para sair\n\n");
    }
    else
    {
        printf("Opcao Invalida\n");
    }

    scanf("%d", &opcao);

   }

    printf("Ate a proxima! ^u^\n");

    return 0;
}
