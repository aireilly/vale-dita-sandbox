# Using Vale with DITA XML

Install `vale` and the `dita-ot`, then open a command prompt and run:

Vale ignores `<codeblock>`, `<tt>`, and `<codeph>` elements by default.

```cmd
vale sync

vale .

 topics/test.dita
 4:10   suggestion  Use sentence-style              RedHat.Headings            
                    capitalization in 'Getting                                 
                    Started'.                                                                                     
 16:43  warning     Do not use end punctuation in   RedHat.HeadingPunctuation  
                    headings.                                                  
 17:10  error       Use 'daemon' rather than        RedHat.TermsErrors         
                    'demon'.  

✖ 1 error, 2 warnings and 15 suggestions in 4 files.

```

Learn more: https://vale.sh/docs/topics/scoping/#dita