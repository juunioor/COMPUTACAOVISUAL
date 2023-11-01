# O que é uma API Gráfica? 

As APIs gráficas são ferramentas especializadas que facilitam a comunicação entre jogos, drivers e placas de vídeo. Elas desempenham um papel crucial ao garantir que jogos funcionem corretamente em hardware de diferentes marcas, como NVIDIA, AMD e Intel. As APIs gráficas atuam como uma ponte entre os motores gráficos dos jogos e os drivers, traduzindo as instruções dos jogos em comandos precisos para o hardware e retornando os resultados aos aplicativos.

**Referências**

https://blog.2amgaming.com/2019/09/o-que-e-api-grafica/

## OpenGL ##

O OpenGL é uma API usada para criar aplicativos que envolvem gráficos em computação. Ela fornece um conjunto de funções específicas para desenvolvedores usarem ao escrever programas em linguagens como C e C++. Embora tenha sido inicialmente projetada com foco em C e C++, ela é eficiente e pode ser aplicada em várias outras linguagens de programação.

O OpenGL é a API gráfica 2D/3D mais amplamente usada na indústria, com amplo suporte e uma abundância de informações disponíveis para ajudar na implementação do OpenGL em hardware e software. Há muitos livros, tutoriais, exemplos de código online, seminários de programação e aulas que documentam a API, extensões, bibliotecas de utilidade e implementações específicas de plataformas, tornando o acesso a informações sobre o OpenGL acessível e econômico.

### Documentação do Pipeline do OpenGL ###

A pipeline do OpenGL, também conhecida como pipeline gráfica, é documentada principalmente através da especificação oficial do OpenGL. Essa especificação descreve detalhadamente o funcionamento de cada etapa da pipeline gráfica, bem como os recursos, funções e comportamentos esperados do OpenGL. A especificação é mantida pelo Consórcio Khronos, responsável pelo desenvolvimento do OpenGL e de outras tecnologias gráficas.

A documentação oficial do OpenGL inclui diversas versões da especificação, cada uma correspondente a uma versão específica do OpenGL. Por exemplo, a especificação do OpenGL 4.6 descreverá a pipeline do OpenGL na versão 4.6.

Essas especificações fornecem informações sobre:

1. **Estados iniciais e padrões**: Descrevem o estado inicial da pipeline e os valores padrão para vários parâmetros e configurações.
2. **Descrição das etapas da pipeline**: Cada etapa da pipeline, como a vertex shader, tessellation, geometry shader, fragment shader, entre outras, é detalhadamente descrita, incluindo os estágios, as entradas e saídas, as operações realizadas e os recursos disponíveis.
3. **Comandos e funções do OpenGL**: A especificação descreve todas as funções e comandos disponíveis no OpenGL, incluindo seus parâmetros e seu comportamento.
4. **Tipos de dados e formatos de textura**: São especificados os tipos de dados suportados e os formatos de textura que podem ser usados nas etapas da pipeline.
5. **Extensões**: Além da funcionalidade principal, a especificação também descreve as extensões disponíveis para estender a funcionalidade do OpenGL.

### Linguagens de shading do OpenGL ###

A linguagem de shading padrão do OpenGL é o GLSL (OpenGL Shading Language), uma linguagem de alto nível que permite a criação de shaders de vértice e fragmento. Além disso, existe o GLSL ES (OpenGL Shading Language for Embedded Systems), uma versão simplificada do GLSL projetada para sistemas embarcados e dispositivos móveis.

O OpenGL também suporta o HLSL quando usado com a extensão de shading "ARB_separate_shader_objects." Esta extensão permite que desenvolvedores utilizem o HLSL no ambiente OpenGL.

Além disso, a linguagem Cg (C for Graphics), desenvolvida pela NVIDIA, é outra opção que pode ser usada no OpenGL para escrever shaders. No entanto, vale ressaltar que a Cg foi descontinuada, e sua utilização diminuiu em favor do GLSL.

### Exemplo de código de shader - Hello World! ###

```
// badprog.com
#include <GL/glut.h>

void displayMe(void)
{
    glClear(GL_COLOR_BUFFER_BIT);
    glBegin(GL_POLYGON);
        glVertex3f(0.0, 0.0, 0.0);
        glVertex3f(0.5, 0.0, 0.0);
        glVertex3f(0.5, 0.5, 0.0);
        glVertex3f(0.0, 0.5, 0.0);
    glEnd();
    glFlush();
}

int main(int argc, char** argv)
{
    glutInit(&argc, argv);
    glutInitDisplayMode(GLUT_SINGLE);
    glutInitWindowSize(300, 300);
    glutInitWindowPosition(100, 100);
    glutCreateWindow("Hello world from Badprog.com :D");
    glutDisplayFunc(displayMe);
    glutMainLoop();
    return 0;
}
```

### Exemplo de aplicação que usa OpenGL ###

O Minecraft, um dos jogos mais populares e influentes do mundo, utiliza o OpenGL como parte fundamental de sua infraestrutura de renderização para criar o ambiente de jogo.

**Referências**

https://www.opengl.org/Documentation/Specs.html

https://www.tecmundo.com.br/video-game/872-o-que-e-opengl-.htm

https://registry.khronos.org/OpenGL/index_gl.php/xml/README.adoc

https://www.badprog.com/c-opengl-hello-world

https://en.wikipedia.org/wiki/List_of_OpenGL_applications
