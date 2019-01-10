# ProCamera
A ProCamera é uma câmera baseada em API Camera2 que realiza as funções comuns da câmera e se esforça para aproveitar o enorme potencial da Camera2, forjando um produto de câmera que é perfeito em função e design.
![camera2](https://github.com/18Gray/ProCamera/blob/master/screenshot/camera2.jpg)
![modeselect](https://github.com/18Gray/ProCamera/blob/master/screenshot/modeselect.jpg)


## Função
1. Funções comuns da câmera: foco automático / medição, foco manual / fotometria, comutação frontal e traseira da câmera, comutação do modo flash, uso de HDR, adição de filtros GPU, ajuste de taxa de disparo, fotografia com lapso de tempo, gravação de vídeo.
2. Processamento de imagem relacionado: Clique no botão no canto inferior esquerdo para inserir o álbum e selecione o álbum para processar a imagem. Incluindo: corte, filtros, legendas, impressões, contraste, etc.

## Em breve para entrar online:
1. Disparo contínuo a 30 fps HD, separação manual da focagem e ponto de medição, 0 disparo do disparador retardado, saída da imagem formatada, ajuste awb / iso / ae.
2. Para o disparo de retrato, a função de reconhecimento de rosto é fornecida e a beleza é executada automaticamente após o reconhecimento ser bem-sucedido.
3. Definir funções relacionadas à interface: incluindo a configuração de nove quadrados, assinatura digital de imagem (posição, tempo, direitos autorais, tamanho da fonte, cor), calibração horizontal, configuração de qualidade de imagem, gravação de qualidade de vídeo, histograma em tempo real,
4. Processamento de imagem: Aproxime-se gradativamente dos snapseed e combine com aplicações interessantes como vsco e prisma.
5. Se o retrato ocupar a maior parte do espaço na imagem, ele usará um processamento de imagem orientado para a beleza, semelhante à bela imagem.

## Uso simples
1. Introduzir o controle Camera2TextureView em xml.
2. Na Atividade ou Fragmento, primeiro defina um caminho para mFile para salvar o endereço da imagem.
3. Em seu onResume, chame cameraTextureView.openCamera () para abrir a câmera.
4. Clique no botão da câmera e ligue para cameraTextureView.takePicture () para completar a foto.
5. Chame cameraTextureView.closeCamera () em onPause para desligar a câmera.

## Uso complexo
O método de uso complicado é, na verdade, baseado no método de uso simples acima, para adicionar a função de ajustar o flash, a comutação frontal e traseira da câmera, configurar HDR, filtrar e assim por diante.
Uma idéia comumente usada aqui é: Depois de clicar no botão no onClick, uma caixa de diálogo Dialog ou PopupWindow irá aparecer, e então a seleção em Dialog ou PopupWindow será clicada, então a mensagem será passada para Camera2Fragment através de EventBus e passada em XXX em Camera2Fragment. O método recebe a mensagem e, em seguida, executa o método cameraTextureView.xxx para executar a operação da câmera correspondente.
Tome a configuração do flash como um exemplo:
1. PopupWindow aparece no onClick.
2. Selecione uma das quatro opções no PopWindow, por exemplo iv_flash_auto, para definir o flash automático, para enviar uma mensagem via EventBus.
3. O onFlashSelect no Camera2Fragment recebe a mensagem, primeiro faz algumas alterações na interface do usuário e, em seguida, cameraTextureView.setFlashMode para definir o modo de flash.

## Importação Gradle


## Confusão de Proguard


## Outros problemas



# ProCamera
ProCamera is a Camera based on Camera2 API, and it implements some common functions about camera. It will excavate the potential of Camera2 API continuously, to forge an impressive product on function and design.
![camera2](https://github.com/18Gray/ProCamera/blob/master/screenshot/camera2.jpg)
![modeselect](https://github.com/18Gray/ProCamera/blob/master/screenshot/modeselect.jpg)
