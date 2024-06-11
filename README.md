**EXPLICACION DEL CODIGO**

**CAPTURA DEL CODIGO**
![](https://i.ibb.co/t8hm31s/PROG.png)

**CODIGO**

package application;
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.GridPane;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Create controls
        Button button = new Button("Button");
        CheckBox checkBox = new CheckBox("CheckBox");
        Hyperlink hyperlink = new Hyperlink("Hyperlink");
        ToggleButton toggleButton = new ToggleButton("ToggleButton");
        RadioButton radioButton = new RadioButton("RadioButton");
        Label label = new Label("Label");
        TextField textField = new TextField();
        textField.setPromptText("some text...");
        PasswordField passwordField = new PasswordField();
        TextArea textArea = new TextArea();
        textArea.setWrapText(true);
        textArea.setText("This is very long text that will wrap to\nseveral lines.");
        ProgressIndicator progressIndicator = new ProgressIndicator(0.49);
        ProgressBar progressBar = new ProgressBar(0.49);
        Slider slider = new Slider();

        // Create layout
        GridPane gridPane = new GridPane();
        gridPane.setHgap(10);
        gridPane.setVgap(10);
        gridPane.setPadding(new Insets(20, 20, 20, 20));

        // Add controls to layout
        gridPane.add(new Label("Button:"), 0, 0);
        gridPane.add(button, 1, 0);

        gridPane.add(new Label("CheckBox:"), 0, 1);
        gridPane.add(checkBox, 1, 1);

        gridPane.add(new Label("Hyperlink:"), 0, 2);
        gridPane.add(hyperlink, 1, 2);

        gridPane.add(new Label("ToggleButton:"), 0, 3);
        gridPane.add(toggleButton, 1, 3);

        gridPane.add(new Label("RadioButton:"), 0, 4);
        gridPane.add(radioButton, 1, 4);

        gridPane.add(new Label("Label:"), 0, 5);
        gridPane.add(label, 1, 5);

        gridPane.add(new Label("TextField:"), 0, 6);
        gridPane.add(textField, 1, 6);

        gridPane.add(new Label("PasswordField:"), 0, 7);
        gridPane.add(passwordField, 1, 7);

        gridPane.add(new Label("TextArea:"), 0, 8);
        gridPane.add(textArea, 1, 8, 2, 1);

        gridPane.add(new Label("ProgressIndicator:"), 0, 9);
        gridPane.add(progressIndicator, 1, 9);

        gridPane.add(new Label("ProgressBar:"), 0, 10);
        gridPane.add(progressBar, 1, 10);

        gridPane.add(new Label("Slider:"), 0, 11);
        gridPane.add(slider, 1, 11);

        // Create scene and show stage
        Scene scene = new Scene(gridPane, 400, 400);
        primaryStage.setTitle("allControls.fxml");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}


**EXPLICACION DEL CODIGO**

- **Importaciones**
package application;
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.geometry.Pos;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.GridPane;
import javafx.scene.layout.HBox;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

Estas líneas importan las clases necesarias de JavaFX para construir la interfaz gráfica, incluyendo controles (como botones y campos de texto) y contenedores de diseño (como GridPane, HBox y VBox).


- **Clase Principal**
public class Main extends Application {

La clase Main extiende Application, lo que convierte a esta clase en una aplicación JavaFX.


- **Método start**
    @Override
    public void start(Stage primaryStage) {

El método start es el punto de entrada para las aplicaciones JavaFX. Aquí es donde se configura y muestra la interfaz de usuario.


- **Creación de controles**
        // Create controls
        Button button = new Button("Button");
        CheckBox checkBox = new CheckBox("CheckBox");
        Hyperlink hyperlink = new Hyperlink("Hyperlink");
        ToggleButton toggleButton = new ToggleButton("ToggleButton");
        RadioButton radioButton = new RadioButton("RadioButton");
        Label label = new Label("Label");
        TextField textField = new TextField();
        textField.setPromptText("some text...");
        PasswordField passwordField = new PasswordField();
        TextArea textArea = new TextArea();
        textArea.setWrapText(true);
        textArea.setText("This is very long text that will wrap to\nseveral lines.");
        ProgressIndicator progressIndicator = new ProgressIndicator(0.49);
        ProgressBar progressBar = new ProgressBar(0.49);
        Slider slider = new Slider();


Se crean instancias de varios controles de JavaFX, como botones (Button), cuadros de texto (TextField), cuadros de verificación (CheckBox), etc. Algunos controles tienen configuraciones adicionales, como TextArea, que tiene el texto ajustado y un texto inicial establecido.


-**Configuración del 'GridPane**
        // Create layout
        GridPane gridPane = new GridPane();
        gridPane.setHgap(10);
        gridPane.setVgap(10);
        gridPane.setPadding(new Insets(20, 20, 20, 20));


Se crea un GridPane, que es un contenedor de diseño que organiza sus hijos en una cuadrícula. Aquí se establecen el espacio horizontal (Hgap) y vertical (Vgap) entre los elementos, y el relleno (padding) alrededor del borde del GridPane.


-**Creación y muestra en escena**
        // Create scene and show stage
        Scene scene = new Scene(gridPane, 400, 400);
        primaryStage.setTitle("allControls.fxml");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

Se crea una Scene con el GridPane como su contenido, y se establece un tamaño de 400x400 píxeles. El Stage principal (primaryStage) se configura con un título y la escena, y luego se muestra con primaryStage.show().



-**Método main**
El método main lanza la aplicación JavaFX llamando a launch(args).


##Resumen
En resumen, este código construye una interfaz gráfica con varios controles organizados en una cuadrícula, y luego muestra esta interfaz en una ventana de 400x400 píxeles.
