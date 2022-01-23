# Extensible CV
This CV uses latex's bibliography references to make extending a CV an easy task. This is very helpful in case you find it hard to keep your CV always updated or you want an easy way to build multiple versions of your CV for different positions.

## Adding positions
In the `main.bbl` file, add a new reference that describes the position, eg:
```
\bibitem{new_position_extended}
\runsubsection{Example GMBH} \descript{Applied Scientist}
\location{May \textbf{2018 } - Present | Berlin, DE}
\newblock  \vspace{-10pt}
\begin{tightemize}
\item Did 1
\item Did 2
\end{tightemize}
```

The id `example_extended` will be how we reference this position in the main cv. The rest should be easy to understand.

## Updating the CV
In `main.tex`, under `Experience` section add the new position as follows:
```
\fullcite{new_position_extended}
\fullcite{old_position1}
\fullcite{old_position2}
\fullcite{old_position3}
\fullcite{old_position4}
```
I like to keep a short and long version of the position to help me customize the CV for different use cases.


## Building the CV
You will need to have Latex compiler so I suggest you try to find a setup guide suitable for your setup to do so. I then use PDFLatex to generate a PDF for my CV.
