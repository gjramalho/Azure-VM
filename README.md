# Laboratório Azure: Documentação do que é o Azure, oque é IaaS, processo de criação de VMs, boas práticas e aprendizado teóricos 
  sobre o uso da platadorma Microsoft Azure

## Oque é Microsoft Azure?
   É uma plataforma de computação em nuvem criada pela Microsoft. Ela oferece uma ampla variedade de  serviços, 
   como hospedagem de aplicações, armazenamento, banco de dados, inteligência artificial, redes e muita mais coisas! Com o Azure, 
   desenvolvedores e empresas podem criar, implantar e gerenciar aplicações em escala global com segurança, flexibilidade e alta 
   disponibilidade! Nesse arquivo REDME iremos comentar mais sobre o recursos de ***Iaas(Infrastructure as a Service )*** e boas 
   práticas.

  ## Criando uma VM-(Maquina Virtual) no Azure

* 1- Começamos criando uma conta no portal do Azure para conseguir ter acesso a criação de VMs.

* 2- Após login criado iremos buscar dentro do portal por _Máquinas virtuais_ na barra de pesquisa do Azure. Após iremos em 
     ***Serviços*** e selecionar ***Máquinas virtuais***, ao entrar na página de máquinas virtuais e selecionar ***Máquina virtual 
     do Azure**. A página ***Criar uma máquina virtual*** é aberta.
     

* 3- Agora iremos começar configurar brevemente algumas coisas, como _Nome da VM_, _Região_ e a img da VM como por exemplo o 
     ***Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2***, após iremos introduzir um nome de usuário e senha (***a senha 
     deve conter no mínimo 12 caracteres***)

* 4- Vamos configurar as ***Regras de porta de entrada***, Iremos selecionar ***Permitir portas selecionadas*** e em seguida, vamos 
     selecionar ***RDP (3389) e HTTP (80)*** na lista suspensa que irá aparecer, Selecione o botão ***Examinar + criar*** na parte 
     inferior esquerda da página. Iremos esperar a execução da validação, e selecionar o botão ***Criar*** na parte inferior 
     esquerda da página.
     

* 5- Após terminar a implantação, vou selecionar ***Ir para o recurso*** e vou começar a etapa de conectar-se á maquina virtual.

## Se conectando à máquina virtual

* 1- Vou clicar em ***Conectar>RDP*** na pág de visão geral da minha VM e nessa mesma guia em ***Conectarse-se ao RDP***, mantenha as 
    opções padrão para se conectar por endereço IP pela porta _3389_ e clicar em ***Baixar arquivo RDP**

* 2- Após fazer o dowload do arquivo RDP vou clicar em ***Conectar*** quando for solicitado. Após vamos na janela de ***Segurança do 
    Windows***, selecione ***Mais opções e Usar uma conta diferente***, Agora vou digitar o usuário como ***localhost\ nome de 
    usúario*** e vou insirir a senha que eu criei para a Máquina virtual, e vou clicar em ***OK***. Durante esse processo eu posso 
    receber um aviso do certificado durante o processo de login é apenas clicar em ***sim*** ou em ***Continuar*** para criar a 
    conexão.
    
 ## Processo de instalação do servidor Web

* 1-  Para vermos a VM em "ação", vou instalar o servidor Web do IIS, vou abrir um Prompt do PowerShell na VM e executar o seguinte 
     comando ***Prestar muita atenção na parte de abrir o PowerShell porque tem que ser aberto exatamente na VM***, e vamos executar 
     o seguinte comando ```Install-WindowsFeature -name Web-Server -IncludeManagementTools ```, quando terminar vou fechar a conexão 
     RDP com a VM.

  ## Exibir a pág de boas-vindas do IIS

* 1-  Essa etapa e mais curta e "Simples". No portal vou selecionar a VM e na visão geral da VM, vou passar o mouse sobre o endereço       de IP para mostrar ***Copiar para área de transferência***. Copiar o endereço de IP e colar em uma guia do navegador.

  ## Desligamento automático da VM

* 1-  para realizar o desligamento autimático da VM  preciso ir na ***Operações da VM***, e selecionar a opção ***Desligamento       
     automático***, após uma página será aberta e vou poder configurar o tempo para o desligamento da VM, terminando de configurar a      hora vou ate ***salvar*** na parte superior para habilitar a config de desligamento automático.

* 2- ***Não esquecer de configurar o fuso horário corretamente para corresponder aos seus requesitos, pq o UTC é a config padrão na          lista suspensa de fuso horario**



## Duvidas que eu tive no processo de entendimento sobre a VM Azure

# Quanto cada disco "aguenta"?---> ***Cada disco de dados pode ter no ate no max 32.767 Gib*** 

# Como eu faço se quiser alterar a letra da unidade do disco temporário?---> ***Eu posso alterar a letra da unidade movendo o   
  arquivo de paginação e reatribuiindo as letras da unidade, mas preciso lembrar de seguir as etapas em uma ordem específica.***

# Requesitos para nome da VM---> ***Deve ter no máximo 15 caracteres***

# 
