/*5) Santa Catarina é conhecida por suas quatro estações bem definidas, o que o torna um estado com alta amplitude térmica (diferença entre a maior e a menor temperatura, registrada em um período). O INMET, Instituto Nacional de Meteorologia, pretende ter os dados de amplitude térmica de uma cidade ou estado. Desenvolva um programa que calcule e mostre os dados diários (segunda à sexta) e a média de amplitude térmica semanal, mostrando os resultados ao final. Exemplo: Digitar o nome da cidade ou estado, perguntar para os cinco dias da semana a maior temperatura do dia e a menor. Mostrar as amplitudes de cada dia e a média.*/
let maxima, maximaSemanal, minima, minimaSemanal, regiao
let temp = 0
let mediaDia
let mediaSemanal
let soma = 0
let cont = 2
let contMaximo = 0, contMinimo = 0

regiao = prompt('Digite sua região que mora ( cidade ou estado ):')
while(cont < 7){
    alert(cont + '°-feira')
    
    maxima = Number(prompt('Digíte a máxima do dia:'))
    minima = Number(prompt('Digíte a mínima do dia:'))
    if(cont == 2){
        maximaSemanal = maxima
        minimaSemanal = minima
        contMaximo = cont
        contMinimo = cont
    }
    
    soma = maxima + minima
    temp += soma
    mediaDia = soma / 2
    alert(`A média de ${cont}°-feira é: ${mediaDia}°C.`)
    
    if(maxima > maximaSemanal){
        maximaSemanal = maxima
        contMaximo = cont
    }
    
    if(minima < minimaSemanal){
        minimaSemanal = minima
        contMinimo = cont
    }
    
    cont++
}

mediaSemanal = temp / 10
alert(`A média da temperatura semanal foi: ${mediaSemanal}°C. A máxima foi na ${contMaximo}°-feira com ${maximaSemanal}°C. A mínima foi na ${contMinimo}°-feira com ${minimaSemanal}°C.`)
