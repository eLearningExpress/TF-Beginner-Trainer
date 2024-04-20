# Einfaches KI-Modell Training für Anfänger mit TensorFlow.js

## Über dieses Projekt

**Diese webbasierte Anwendung von e-Learning Express ermöglicht es Anfängern, ein einfaches künstliches Intelligenzmodell zu trainieren <u>und zu visualisieren</u>.** Sie nutzt TensorFlow.js zur Modellerstellung und -training. 

**[TensorFlow.js](https://www.tensorflow.org/js)** ist eine JavaScript-Bibliothek, die es ermöglicht, maschinelles Lernen direkt im Browser oder in einer Node.js-Umgebung zu betreiben. Sie ist ein Teil des breiteren TensorFlow-Ökosystems, das von Google entwickelt wurde (eingeführt im März 2018). 

>  TensorFlow.js ermöglicht es Entwicklern, Modelle des maschinellen Lernens zu trainieren und zu nutzen, ohne dass Benutzer Software installieren müssen oder die Daten den Browser verlassen.

Neben TensorFlow.js gibt es eine Reihe weiterer Bibliotheken und Frameworks, die zur Entwicklung und Implementierung von maschinellem Lernen verwendet werden können. Einige der bekanntesten sind: [PyTorch](https://pytorch.org/), [Scikit-learn](https://scikit-learn.org/stable/), [Keras](https://keras.io/), [Microsoft Cognitive Toolkit (CNTK)](https://learn.microsoft.com/de-de/cognitive-toolkit/), [Deeplearning4j](https://deeplearning4j.konduit.ai/), [ONNX (Open Neural Network Exchange)](https://onnx.ai/) und [Fast.ai](https://www.fast.ai/).



>  **Diese Anwendung ist darauf ausgelegt, Benutzern ein grundlegendes Verständnis des maschinellen Lernens zu vermitteln, indem sie interaktive Elemente zur Durchführung und Beobachtung des Trainingsprozesses bietet.**



## Grundlegende Begriffe

-  **Epoche**: Eine Epoche im Kontext des maschinellen Lernens bezeichnet einen kompletten Durchlauf durch den gesamten Trainingsdatensatz, den das Modell einmal komplett gesehen hat. Mehrere Epochen beim Training können dem Modell helfen, besser zu lernen und die Genauigkeit der Vorhersagen zu verbessern.
-  **Trainingsverlust**: Der Trainingsverlust ist ein Maß dafür, wie gut das Modell die Trainingsdaten während des Trainingsprozesses anpasst. Ein hoher Verlust weist darauf hin, dass das Modell die Daten schlecht vorhersagt, während ein sinkender Verlust darauf hindeutet, dass das Modell sich verbessert und die Daten zunehmend besser vorhersagen kann.
-  **Netzwerkparameter**: Sind die Parameter innerhalb eines neuronalen Netzwerks, die angepasst werden, um die Vorhersagegenauigkeit des Modells zu optimieren. Diese Parameter werden im Training durch Algorithmen wie den Gradientenabstieg kontinuierlich angepasst, um den Verlust zu minimieren.



## Voreingestellte Trainingsdaten

Die Anwendung verwendet zwei vordefinierte Arrays für das Training:

-  **xs (Eingabedaten)**: `[-1.0, 0.0, 1.0, 2.0, 3.0, 4.0]` repräsentieren die Eingabewerte, mit denen das Modell trainiert wird.
-  **ys (Zieldaten)**: `[-3.0, -1.0, 1.0, 3.0, 5.0, 7.0]` sind die entsprechenden Ausgabewerte, die das Modell zu vorhersagen versucht. Diese Daten zeigen die Beziehung zwischen den Eingabewerten und den Ausgaben, die das Modell lernen soll.

Diese Datensätze dienen als Grundlage für das Modell, um eine lineare Beziehung zu lernen, die es ihm ermöglicht, auf Basis der Eingaben genaue Vorhersagen zu treffen.



## Hauptfunktionen

-  **Training starten**: Automatisches Durchlaufen aller Trainingsepochen. Je öfter man Trainingsepochen durchläuft, desto genauer kann das Modell  die zugrundeliegenden Muster in den Trainingsdaten erkennen und somit  seine Vorhersagegenauigkeit verbessern.
-  **Schritt-für-Schritt-Training**: Ermöglicht das Training des Modells Schritt für Schritt durch jede Epoche.
-  **Verlustdiagramm anzeigen**: Zeigt den Trainingsverlust nach jeder Epoche an, um die Verbesserung der Modellgenauigkeit zu veranschaulichen.
-  **Anzeige der Netzwerkparameter**: Aktualisiert und zeigt die Netzwerkparameter des Modells nach jedem Trainingsschritt an. Netzwerkparameter, oft als Gewichte und Biases bezeichnet, sind die  Schlüsselvariablen in einem neuronalen Netzwerk, die während des  Trainingsprozesses angepasst werden, um die Leistung des Modells auf  Basis der verfügbaren Daten zu optimieren.
-  **Vorhersagen durchführen**: Erlaubt es Benutzern, Vorhersagen basierend auf Eingabewerten zu generieren.
-  **Modal für Vorhersageergebnisse**: Zeigt das Ergebnis einer Vorhersage in einem Pop-up-Fenster an.



## Anleitung zur Benutzung

1. **Webseite öffnen**: Laden Sie die HTML-Seite in Ihrem Browser.
2. **Training starten**: Klicken Sie auf „Start Training“, um das Modell mit den voreingestellten Daten zu trainieren.
3. **Trainingsfortschritt beobachten**: Überwachen Sie den Verlauf des Trainingsverlusts im Diagramm, das sich mit jeder Epoche aktualisiert.
4. **Schrittweises Training nutzen**: Verwenden Sie „Trainiere Schritt für Schritt“, um das Modell schrittweise zu trainieren und dabei die internen Veränderungen zu beobachten.
5. **Vorhersage machen**: Geben Sie einen X-Wert in das entsprechende Feld ein und klicken Sie auf „Vorhersagen“, um den vorhergesagten Y-Wert zu erhalten nachdem das Modell trainiert wurde.
6. **Ergebnis überprüfen**: Überprüfen Sie das Vorhersageergebnis, das im Modal-Fenster angezeigt wird.



## Technische Details

-  **TensorFlow.js**: Wird für das Erstellen und Trainieren des neuronalen Netzwerks verwendet.
-  **Chart.js**: Dient der Visualisierung der Daten in Form von Diagrammen.
-  **Tailwind CSS**: Sorgt für das responsive Design der Benutzeroberfläche.



### HTML-Struktur

Die Webseite enthält mehrere Hauptelemente:

-  **Diagramme**: Zwei `<canvas>` Elemente für die grafische Darstellung des Trainingsverlaufs und der Vorhersagen.
-  **Bedienelemente**: Buttons zum Starten des Trainings, zum schrittweisen Trainieren und zum Durchführen von Vorhersagen.
-  **Eingabefelder**: Ein Textfeld zur Eingabe der X-Werte für Vorhersagen.
-  **Statusanzeigen**: Textelemente zur Anzeige des Trainingsstatus und der aktuellen Netzwerkparameter.



### JavaScript-Funktionen

Das Skript regelt die Interaktionen innerhalb der Anwendung, einschließlich:

-  **Modellkonfiguration und Training**,
-  **Aktualisierung der Diagramme und Netzwerkparameteranzeigen**,
-  **Handhabung von Benutzereingaben und Vorhersagen**.



>  Diese einfache Einführung in die Welt des maschinellen Lernens soll Benutzern helfen, grundlegende Konzepte und Prozesse zu verstehen und anzuwenden.