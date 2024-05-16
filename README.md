# Desafio Dio - Projeto de Automação por meio de Comando de Voz

# **Parte 1**

A automação por comando de voz é uma tecnologia que permite aos usuários controlar dispositivos e realizar tarefas usando comandos de voz falados. Este projeto visa criar um sistema de automação de voz robusto e bem projetado que atenda às necessidades específicas dos usuários.

## **Requisitos**

- Reconhecimento de voz preciso

- Suporte para uma ampla gama de comandos

- Capacidade de controlar vários dispositivos

- Interface de usuário intuitiva

- Segurança e privacidade

  

## **Arquitetura do Sistema**

O sistema de automação de voz será composto pelos seguintes componentes:

- **Módulo de Reconhecimento de Voz:** Responsável por converter comandos de voz falados em texto.

- **Módulo de Processamento de Linguagem Natural (PNL):** Analisa o texto do comando de voz e extrai a intenção e os parâmetros do usuário.

- **Módulo de Controle de Dispositivo:** Envia comandos aos dispositivos conectados para executar as tarefas solicitadas.

- **Interface de Usuário:** Permite aos usuários interagir com o sistema, fornecer comandos e receber feedback.

  

## **Recursos**

O sistema de automação de voz fornecerá os seguintes recursos:

- **Reconhecimento de Voz Preciso:** Usando algoritmos avançados de aprendizado de máquina, o sistema reconhecerá comandos de voz com alta precisão, mesmo em ambientes ruidosos.

  

- **Suporte para Ampla Gama de Comandos:** O sistema suportará uma ampla gama de comandos de voz, incluindo comandos para controlar dispositivos, obter informações e executar tarefas.

  

- **Controle de Vários Dispositivos:** O sistema permitirá aos usuários controlar vários dispositivos conectados, como luzes, termostatos e eletrodomésticos.

  

- **Interface Intuitiva:** O sistema terá uma interface de usuário intuitiva que permitirá aos usuários interagir facilmente com o sistema e fornecer comandos.

  

- **Segurança e Privacidade:** O sistema implementará medidas de segurança robustas para proteger a privacidade dos usuários e impedir o acesso não autorizado.

  

## **Implementação**

O sistema de automação de voz será implementado usando uma combinação de tecnologias, incluindo:

- **Bibliotecas de Reconhecimento de Voz:** Bibliotecas de código aberto, como Kaldi e CMU Sphinx, serão usadas para reconhecimento de voz.

  

- **Bibliotecas de PNL:** Bibliotecas de PNL, como NLTK e spaCy, serão usadas para processamento de linguagem natural.

  

- **APIs de Controle de Dispositivo:** APIs fornecidas por fabricantes de dispositivos serão usadas para controlar dispositivos conectados.

  

- **Estrutura de Interface de Usuário:** Uma estrutura de interface de usuário, como React ou Vue.js, será usada para criar a interface de usuário.

  

## **Benefícios**

O sistema de automação de voz fornecerá os seguintes benefícios aos usuários:

- **Conveniência:** Os usuários podem controlar dispositivos e realizar tarefas sem usar as mãos.
- **Eficiência:** O sistema pode automatizar tarefas repetitivas, economizando tempo e esforço dos usuários.
- **Acessibilidade:** O sistema pode ser usado por pessoas com deficiências que podem ter dificuldade em usar interfaces tradicionais.
- **Segurança:** O sistema pode melhorar a segurança da casa, permitindo aos usuários controlar dispositivos remotamente.





### O prgrama arduino e estrutura projeto comando de voz, com plataforma e software



O programa Arduino para o projeto de comando de voz é relativamente simples. basta instalar a biblioteca de voz V3, encontrada no site da Arduino. Depois disso, criar um novo projeto Arduino e incluir a biblioteca de voz V3 em seu código. e criar uma função de escuta que monitorará o microfone do Arduino e detectará quando uma palavra-chave específica é dita. 

Quando uma palavra-chave é detectada, sua função de escuta pode enviar um sinal para o seu Arduino. usar esse sinal para executar qualquer ação que desejar, como ligar uma luz, desligar uma luz ou reproduzir um som.

A estrutura do seu projeto de comando de voz depende do seu objetivo final. 

Por exemplo, se você deseja controlar dispositivos domésticos inteligentes,  usar uma plataforma como o Home Assistant ou o SmartThings. 

Estas plataformas permitem que você controle dispositivos domésticos inteligentes usando comandos de voz. Se deseja criar um aplicativo de comando de voz, usar uma plataforma como o Android Studio ou o Xcode. 

Estas plataformas permitem que você crie aplicativos para dispositivos móveis que podem usar comandos de voz.

Independentemente do seu objetivo final, o software para o seu projeto de comando de voz dependerá das ferramentas e plataformas. No entanto, existem algumas ferramentas e plataformas que são mais populares do que outras. 

Aqui estão algumas das ferramentas e plataformas mais populares para o desenvolvimento de projetos de comando de voz:

- **Arduino:** 

  A Arduino é uma plataforma de prototipagem de hardware de código aberto que é usada para criar projetos de automação e controle. A Arduino possui uma biblioteca de voz V3 que pode ser usada para criar projetos de comando de voz.

  

- **Home Assistant:** 

- O Home Assistant é uma plataforma de automação residencial de código aberto que é usada para controlar dispositivos domésticos inteligentes. O Home Assistant possui um suporte integrado para comandos de voz, o que significa que você pode controlar seus dispositivos domésticos inteligentes usando comandos de voz.

  

- **SmartThings**: 

  O SmartThings é uma plataforma de automação residencial de código aberto que é usada para controlar dispositivos domésticos inteligentes. O SmartThings possui um suporte integrado para comandos de voz, o que significa que você pode controlar seus dispositivos domésticos inteligentes usando comandos de voz.

  

- **Android Studio**: 

  O Android Studio é um ambiente de desenvolvimento integrado (IDE) para desenvolvimento de aplicativos Android. O Android Studio possui um suporte integrado para comandos de voz, o que significa que você pode criar aplicativos para dispositivos móveis que podem usar comandos de voz.

  

- **Xcode:** O Xcode é um ambiente de desenvolvimento integrado (IDE) para desenvolvimento de aplicativos iOS. O Xcode possui um suporte integrado para comandos de voz, o que significa que você pode criar aplicativos para dispositivos móveis que podem usar comandos de voz.



### PROGRAMA RECONHECIMENTO DE VOZ ARDUINO

O programa abaixo usa a biblioteca de voz V3 da Arduino para reconhecer comandos de voz e executar ações correspondentes. O código usa o microfone do Arduino para capturar o áudio e a biblioteca de voz V3 para analisar o áudio e identificar os comandos de voz. Quando um comando de voz é identificado, o código executa a ação correspondente.



```plaintext
#include <Arduino.h>
#include <VoiceV3.h>

// Define a função que será executada quando um comando de voz é identificado
void executarComando(String comando) {
  // Se o comando é "ligar a luz", ligue a luz
  if (comando == "ligar a luz") {
    digitalWrite(LED_BUILTIN, HIGH);
  }
  // Se o comando é "desligar a luz", desligue a luz
  else if (comando == "desligar a luz") {
    digitalWrite(LED_BUILTIN, LOW);
  }
}

// Inicialize o microfone do Arduino
VoiceV3 microfone;

void setup() {
  // Inicialize o serial monitor
  Serial.begin(9600);

  // Inicialize o microfone do Arduino
  microfone.begin();
}

void loop() {
  // Capture o áudio do microfone
  int16_t audio[1024];
  int tamanhoAudio = microfone.lerAudio(audio);

  // Analise o áudio e identifique os comandos de voz
  String comando = microfone.identificarComando(audio, tamanhoAudio);

  // Se um comando de voz foi identificado, execute a ação correspondente
  if (comando != "") {
    executarComando(comando);
  }
}
```

Para executar este programa, você precisará instalar a biblioteca de voz V3 da Arduino. Você pode encontrar instruções sobre como instalar a biblioteca no site da Arduino. Depois de instalar a biblioteca, você poderá carregar o código no seu Arduino. Quando o código estiver carregado, você poderá falar os comandos de voz e o Arduino executará as ações correspondentes.0



import speech_recognition as sr
import os



# Função para reconhecimento de voz

def reconhecimento_voz():
    # Inicializa o reconhecedor
    reconhecedor = sr.Recognizer()

    with sr.Microphone() as source:
        print("Diga algo...")
        
        # Ajusta para o ruído ambiente
        reconhecedor.adjust_for_ambient_noise(source)
        
        # Escuta o áudio do microfone
        audio = reconhecedor.listen(source)
    
    try:
        # Reconhece o áudio usando a API do Google
        texto = reconhecedor.recognize_google(audio, language='pt-BR')
        print("Você disse: ", texto)
        return texto.lower()
    except sr.UnknownValueError:
        print("Não foi possível entender o áudio")
        return ""
    except sr.RequestError as e:
        print("Erro ao solicitar resultados; {0}".format(e))
        return ""



# Função para abrir aplicativos com base no comando de voz



def abrir_aplicativo(comando):
    if "excel" in comando:
        os.system("start excel")
    elif "navegador" in comando:
        os.system("start chrome")
    elif "word" in comando:
        os.system("start winword")
    elif "powerpoint" in comando:
        os.system("start powerpnt")
    else:
        print("Aplicativo não reconhecido")



# Função principal


def main():
    print("Bem-vindo ao sistema de automação por reconhecimento de voz!")
    print("Você pode dizer 'sair' a qualquer momento para encerrar o programa.")
    print("--------------------------------------------------------")

    while True:
        comando = reconhecimento_voz()
    
        if "sair" in comando:
            print("Encerrando o programa...")
            break
    
        abrir_aplicativo(comando)

if __name__ == "__main__":
    main()





# **Parte2**



# voice-recognition-automation

![Logo](https://firebasestorage.googleapis.com/v0/b/storage-1cbb2.appspot.com/o/Minimalist-BannerV2.png?alt=media&token=27299998-acf5-4edb-a34b-862622bf4718)

## Descrição
Automação com reconhecimento de voz em Python utilizando as bibliotecas pyttsx3, subprocess, pyaudio e speech_recognition envolve a criação de um programa que permite a interação com o computador por meio de comandos de voz.

## Instalação
Certifique-se de ter o Python instalado em seu sistema. Você pode verificar digitando o seguinte comando no prompt de comando ou terminal:

### `python --version`

Certifique-se de ter uma versão igual ou superior à 3.6.

## Instalação do SpeechRecognition
Para instalar a biblioteca SpeechRecognition, execute o seguinte comando no prompt de comando ou terminal:

### `pip install SpeechRecognition`

Isso instalará a biblioteca SpeechRecognition em seu ambiente Python.

## Instalação do Pyttsx3
Para instalar a biblioteca Pyttsx3, execute o seguinte comando no prompt de comando ou terminal:

### `pip install pyttsx3`

## Instalação do PyAudio
A biblioteca PyAudio requer algumas dependências extras para funcionar corretamente. Siga as instruções abaixo com base no seu sistema operacional:

## Windows
* Instale o Visual Studio C++ Build Tools. Você pode baixá-lo no site oficial da Microsoft.
* Em seguida, instale o PyAudio executando o seguinte comando:

### `pip install PyAudio`

## macOS
* Instale o PortAudio usando o Homebrew, um gerenciador de pacotes para macOS. Se você ainda não tem o Homebrew, você pode instalá-lo executando o seguinte comando:

### `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

* Em seguida, instale o PortAudio com o seguinte comando:

### `brew install portaudio`
* Agora você pode instalar o PyAudio executando o seguinte comando:

### `pip install PyAudio`

## Linux (Debian/Ubuntu)
* Execute o seguinte comando para instalar o PortAudio:

## arduino

### `sudo apt-get install portaudio19-dev`

* Em seguida, você pode instalar o PyAudio com o seguinte comando:

### `pip install PyAudio`

<br/>

Após seguir essas etapas, você terá o SpeechRecognition e o PyAudio instalados em seu ambiente Python e poderá usá-los. Certifique-se de importar as bibliotecas corretamente em seus scripts para utilizá-las.



## **Conclusão**

Este Projeto de Automação por Comando de Voz visa criar um sistema robusto e bem projetado que atenda às necessidades dos usuários. O sistema fornecerá reconhecimento de voz preciso, suporte para uma ampla gama de comandos, controle de vários dispositivos, interface intuitiva e segurança e privacidade. Ao implementar este sistema, os usuários podem desfrutar dos benefícios da conveniência, eficiência, acessibilidade e segurança.



