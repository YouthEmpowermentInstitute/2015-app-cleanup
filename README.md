This repo is here so that I can clean the code and do some light version control.

### Cleaning the Popups
The popups make up the bulk of the code, but they're all out of whack indentation-wise. The below regex mostly fixed them. I can't tell why some aren't matched.


##### Search Pattern
`
[^<]*(<div\sdata-role="popup"\sid="[^"]*"\sclass="ui-content">\n)[^<]*(<h3>[^<]*</h3>\r)[^<]*(<p>[^<]*</p>\r)[^<]*(<div\sclass="ui-grid-b">\r)[^<]*(<div\sclass="ui-block-a"></div>\r)[^<]*(<div\sclass="ui-block-b"><a\shref="#"\sclass="ui-btn\sui-corner-all\sui-shadow"\sdata-rel="back">[^>]*</a></div>\r)[^<]*(<div\sclass="ui-block-c"></div>\r)[^<]*(</div>\r)[^<]*(</div>\r)`

##### Replace Pattern
`\t\t\1\t\t\t\2\t\t\t\3\t\t\t\t\4\t\t\t\t\t\5\t\t\t\t\t\6\t\t\t\t\t\7\t\t\t\t\8\t\t\9\r`

