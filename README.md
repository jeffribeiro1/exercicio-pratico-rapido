EXERCÍCIO PRÁTICO RÁPIDO

Aluno: Jefferson Santino Ribeiro Complete o código abaixo:

typescript

// 1. Crie um tipo literal para cor com: "vermelho", "azul", "verde" type Cor = "vermelho " | "azul" | "verde";

ATENÇÃO CUIDADO COM OS ESPAÇOS NOS STRINGS "vermelho''
// 2. Crie um tipo Carro com:

// - marca (string, readonly)

// - modelo (string)

// - cor (do tipo Cor acima)

// - ano? (opcional, number)

type Carro = {

readonly marca: string; // Nunca pode mudar

modelo: string; // Pode mudar

cor: string; // Pode mudar

ATENÇÃO você usou cor: string em vez de cor: Cor. Quando criamos um tipo customizado, devemos usá-lo! O exercício pede especificamente para usar o tipo Cor ano? : number; // Opcional
};

const Carro = { marca: "Fiat",

modelo : "Uno", cor: "vermelho", ano : 2010

};

// 3. Crie uma função Generic que retorne o primeiro elemento de um array function primeiro<T>(array: T[]): T {

ATENÇÃO: Se o array estiver VAZIO: array[0] retorna undefined, mas prometemos retornar sempre T então ❌ BUG: Promessa quebrada
Ficaria:

function primeiro<T>(array: T[]): T | undefined {

return array[0];

}

O undefined é como um aviso honesto que diz: "Ei, pode ser que não tenha nada aqui!"
return array [0];

}
