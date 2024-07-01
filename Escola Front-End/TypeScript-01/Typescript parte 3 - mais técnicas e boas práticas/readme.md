Mikio Nishiya
Curso concluído em 25/05/2024

Tópicos:
    ENTENDENDO DECORATORS
    1- Introdução e estrutura do projeto
    2- Requisitos não funcionais
    3- Decorator de método
    4- Logar tempo de execução com decorator

    DECORATORS DE MÉTODOS
    1- Decorator com parâmetro
    2- Criação de um decorator de inspeção
    3- Ordem de execução dos decorators
    4- Simplificação no design de decorators
    5- Portabilidade de funcionalidade antiga para decorators

    DECORATOR DE PROPRIEDADE
    1- Como evitar código duplicado
    2- Decorator de propriedade
    3- Criação dinâmica de getters
    4- O uso de Object.defineProperty
    5- Cache de decorators




Anotações:
/* -- [ MODELO DE DECORATOR ] ------
export function nomeDaFuncao() {
    return function (target: any, propertyKey: string, descriptor: PropertyDescriptor) {
        const metodoOriginal = descriptor.value;

        descriptor.value = function (...args: any[]) {
            const retorno = metodoOriginal.apply(this, args)

            /// toDo

            return retorno;
        }

        return descriptor;
    }
}
*/