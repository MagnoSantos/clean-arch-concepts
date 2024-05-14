# clean-arch-concepts

Clean Architecture 
Arquitetura de software é um tema que tem despertado bastante interesse, pois independente do tamanho da equipa (seja um único membro, construção de uma startup, ou múltiplas equipas trabalhando em paralelo em grandes projetos) deve-se sempre considerar a arquitetura a ser adotada, visando escalonamento, que o software seja robusto e flexível. 
Um código não tolerável a mudanças, dificulta consideravelmente a implementação de novos requisitos necessários para tua evolução, e consequentemente a sua manutenção. 

Clean Architecture foi primeiramente apresentado em The Clean Code Blog de Uncle Bob e posteriormnete no ano de 2017 a arquitetura foi promovida no livro Clean Architecture: A Crafsman's Guide To Software Structure. 

Mas o que é?

Clean Architecture é uma arquitetura de software proposta por Robert Cecil Martin que tem por objetivo padronizar e organizar o código desenvolvido, favorecer sua reusabilidade, assim como independência tecnológica. 
Domain Centric Architectures: arquiteturas centradas no dominio
Ao estudar Clean Architecture, em algum momento, depara-se com alguma outra arquitetura de design similar, que visa isolar o core da aplicação do mundo externo através do uso de camadas, o princípio de Separação de Responsabilidades (Separation of Concerns - SoC).
Por exemplo: 
- Haxagonal Architecture (conhecido como Ports and Adapters)
- Onion Architecture
Ambos tem como ponto comum colocar o domínio no centro da arquitetura. 
Entender a infraestrutura por trás da Arquitetura Limpa

![image](https://github.com/MagnoSantos/clean-arch-concepts/assets/20459937/5e3034de-31fd-433f-9d54-82ebf2208f7b)

Arquitetura de camadas (Layered Architecture), onde as setas esboçam a direção das dependências seguindo um fluxo do topo para baixo. Assim, a interface de usuário depende da camada de domínio, que por sua vez depende da camada de acesso ao banco de dados. Existindo um forte acoplamento entre as camadas, de forma que, para substituir a camada de banco de dados eventualmente precisamos alterar a camada de domínio. 

![image](https://github.com/MagnoSantos/clean-arch-concepts/assets/20459937/334cfb17-0d62-4bc1-9a1c-1cd8db585524)
 
Uma vez que a organização do projeto tem de ser fácil entendimento e principalmente acompanhar metodologias ágeis para ser factível a mudanças, conforme as necessidades encontradas no amadurecimento do software, o fluxo acima altera as dependências entre as camadas, a centralizar a camada de domínio com uma alteraçã na seta que liga a camada de domínio com a de acesso à base de dados. 
Portanto, já temos uma vantagem da Clean Architecture em comparação com as arquiteturas tradicionais de três camadas, essencialmente poder definir os componentes de infraestrutura em um momento posterior, assim como removê-los ou substituí-los com uma complexidade reduzida. Portanto, projetar aplicativos com menor acoplamente e independentes de detalhes técnicos de implementação, como banco de dados e estruturas. 
Clean Architecture: mais que camadas
- Domínio: contém toda a lógica de negócio, o núcleo aqui deve ser responsável pela razão do software existir, ou seja, o domínio entrega a identidade do seu aplicativo. Alterações aqui podem portanto modificar a essência do sotware. 
- Infrastructure: responsável por identificar como o software se comunica com o mundo externo, por exemplo a abrir a comunicação a humanos, através de uma interface visual, ou comunicação a um banco de dados, filas e até mesmo integração com outras APIs. 

![image](https://github.com/MagnoSantos/clean-arch-concepts/assets/20459937/092642bb-2eb2-406d-8285-6abd2b76366a)

 ![image](https://github.com/MagnoSantos/clean-arch-concepts/assets/20459937/c313d62d-1649-46aa-b206-c9f64a002bec)

Por que separar em camadas?
Partindo do princípio de que está regra de dependência está sendo bem aplicada, a separação visa nos poupar de problemas futuros com a manutenção do software, deixando, inclusive, o sistema completamente testável, pois as regras são testadas sem necessariamente envolver interface do usuário, banco de dados, servidor ou qualquer elemento externo. 
Outro ponto de extrema relevância, por ser uma arquitetura de software amplamente independente, é a que a princípio conseguimos fazer a substituição da interface do usuário sem que isto reflita no resto do sistema. 


