# tikz-uml v1.0b

The original package contains a bug at line 629 where there is the statement

<pre><code>\pgfmathsetmacro{\weightT}{1-\real{\weight}</code></pre>

Using once of the different types of <code>umlrelation</code> to link different classes, you get this error

<pre><code>! Undefined control sequence.
\pgfmath@dimen@ ...men@@ #1=0.0pt\relax \pgfmath@</code></pre>

The problem with it is the use of <code>\real</code>, which has been moved to other macro in the new viersion of <code>pgfmathparses</code> as reported in [this question on TeX-StackExchange](http://tex.stackexchange.com/questions/263174/undefined-control-sequence-error-when-using-tikz-uml-package-in-latex "Undefined control sequence error when using tikz-uml package")