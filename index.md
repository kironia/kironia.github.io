---
layout: default
title: Windsurfen-Ecke von Stagyrit
---

<header>
    <h1>Windsurfen-Ecke von Stagirit</h1>
</header>
<details open>
    <summary>
        <h2>Über den Kanal</h2>
    </summary>
    <p>
        Windsurfen ist besser als uralte Computerspiele. Aber Sie können doch nie die Lösung selber finden. 
    </p>
</details>
{% include computerspiel.html title="Windsurfen-Ecke" description="Es ist eine Windsurfen-Ecke oder das Geheimnis der Nostalgie-Ecke von Stagirit. Ich kann nicht windsurfen, aber ich bin Oracle-zertifizierter Java-Entwickler. Außerdem, Windsurfen ist mir ein bisschen zu langweilig." path="RvTsRlO182I" si="B6Xya-7JI8zIsm0t" %}
{% include computerspiel.html title="Koloriert Windsurfen-Ecke" description="Es war ein bisschen teuer, aber ich hatte das koloriert. Es ist noch ein Geheimnis der Nostalgie-Ecke von Stagirit." path="8t6f-HbpXvk" si="dblfoDFs3uZd_6Zm" %}
{% include computerspiel.html title="Call of Cthulhu: Shadow of the Comet" description="Man kann produktiver sein, als diese Videospiele zu spielen. 🏄  Zum Beispiel kann man Windsurfen lernen. Zumindest sollte man diese alten Videospiele nicht beenden. Diesmal ist es nicht beendet, trotzdem schenke ich es Ihnen." path="9cNXbYJlFEI" si="dnrmqyskVZ5l1ApM" %}

<details open>
    <summary>
        <h2>Kontakt</h2>
    </summary>
    <a href="images/bigger-avatar.png"><img alt="" class="u-photo" src="images/avatar.png"></a>
    <ul>
        <li class="p-name fn">
            <span class="p-given-name">Maciej Matiaszowski</span>
        </li>
{% include url.html header="Email" url="mailto:maciej.matiaszowski@gmail.com?subject=Nostalgie-Ecke%20von%20Stagirit" title="Email me" name="maciej.matiaszowski@gmail.com" %}
{% include url.html header="Gitter" url="https://matrix.to/#/#kassette:gitter.im" title="Gitter &#124; Kassette" name="#kassette" %}
{% include url.html header="Homepage" url="https://Stagyrite.GitHub.io/" title="Maciej Matiaszowski &#124; Stagyrite" name="Stagyrite.GitHub.io" %}
{% include url.html header="GitHub" url="https://github.com/Stagyrite/" title="Stagyrite (Maciej Matiaszowski)" name="GitHub/Stagyrite" %}
    </ul>
</details>

<details>
    <summary>
        <h3>Sprechen Streem</h3>
    </summary>
    <h4>./<a class="u-url url" href="https://stagyrite.github.io/streemdox/" title="Streem documentation project &#124; Streemdox" rel="me">streem</a> <a class="u-url url" href="https://github.com/kironia/kironia.github.io/blob/main/S%C3%BC%C3%9Figkeitenspiel.strm" title="kironia.github.io/Süßigkeitenspiel.strm at main · kironia/kironia.github.io" rel="me">Süßigkeitenspiel.strm</a></h4>
    <pre>
gewünschtesErgebnis = (spieler) -> {
    spieler + " gewinnt"
}

gegenteiliges = (spieler) -> {

    if (spieler == "A") {
        "B"
    } else {
        "A"
    }

}

beendenFallsUngültig = (spieler, süßigkeiten) -> {

    if (süßigkeiten > 50) {
        print("zu viele Süßigkeiten")
        exit(1)
    } else if (süßigkeiten < 1) {
        print("Die Anzahl der Süßigkeiten muss positiv sein.")
        exit(1)
    } else if (spieler != "A") {
    
        if (spieler != "B") {
            print("Der Spieler muss entweder 'A' oder 'B' sein.")
            exit(1)
        }
        
    }

}

spielen = {

    case _, 1 -> ergebnis = "das Remis" #  Wenn nur noch ein Bonbon übrig ist, endet das Spiel unentschieden.
    case spieler, 2 -> gewünschtesErgebnis(spieler) # Ich kann sie alle essen.
    case spieler, 3 -> gewünschtesErgebnis(spieler) # ebenso
    case spieler, süßigkeiten ->
        beendenFallsUngültig(spieler, süßigkeiten)
        basisergebnis = spielen(gegenteiliges(spieler), süßigkeiten - 2)

        if (basisergebnis == "das Remis") {
            # Es dürfte ein Unentschieden werden.
            remisErgebnis = spielen(gegenteiliges(spieler), süßigkeiten - 3)
                   
            if (gewünschtesErgebnis(spieler) == remisErgebnis) {
                # Ich möchte nicht, dass der andere Spieler gewinnt.
                ergebnis = remisErgebnis
            } else {
                # Es ist ein Remis.
                ergebnis = basisergebnis
            }
                    
        } else if (basisergebnis == gewünschtesErgebnis(spieler)) {
            # Der Spieler ist mit dem Ergebnis zufrieden.
            ergebnis = basisergebnis
        } else {
            # Ich möchte gewinnen, aber der andere Spieler gewinnt.
            ergebnis = spielen(gegenteiliges(spieler), süßigkeiten - 3)
        }

}

seq(10) | { süßigkeiten -> spielen("A", süßigkeiten) } | stdout

# Output
# das Remis
# A gewinnt
# A gewinnt
# das Remis
# B gewinnt
# das Remis
# A gewinnt
# A gewinnt
# das Remis
# B gewinnt
</pre>

</details>

<footer>⬛⬜🚢⏳</footer>
