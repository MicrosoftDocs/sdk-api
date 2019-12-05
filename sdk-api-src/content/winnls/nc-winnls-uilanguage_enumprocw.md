---
UID: NC:winnls.UILANGUAGE_ENUMPROCW
title: UILANGUAGE_ENUMPROCW (winnls.h)
description: An application-defined callback function that processes enumerated user interface language information provided by the EnumUILanguages function.
old-location: intl\enumuilanguagesproc.htm
tech.root: Intl
ms.assetid: 5890bde9-7089-4440-a9cf-04b502183770
ms.date: 12/05/2018
ms.keywords: EnumUILanguagesProc, UILANGUAGE_ENUMPROC, UILANGUAGE_ENUMPROC callback, UILANGUAGE_ENUMPROC callback function [Internationalization for Windows Applications], UILANGUAGE_ENUMPROCA, UILANGUAGE_ENUMPROCW, _win32_EnumUILanguagesProc, intl.enumuilanguagesproc, winnls/UILANGUAGE_ENUMPROC
ms.topic: callback
f1_keywords:
- winnls/UILANGUAGE_ENUMPROC
dev_langs:
- c++
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winnls.h
api_name:
- UILANGUAGE_ENUMPROC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UILANGUAGE_ENUMPROCW callback function


## -description


An application-defined callback function that processes enumerated user interface language information provided by the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a> function. The UILANGUAGE_ENUMPROC type defines a pointer to this callback function. <b>EnumUILanguagesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - lParam [in]

Application-defined value.


#### - lpUILanguageString [in]

Pointer to a buffer containing a null-terminated string representing a user interface language identifier or language name, depending on the value for the <i>dwFlags</i> parameter passed in the call to <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a>.


## -returns



Returns <b>TRUE</b> to continue enumeration or <b>FALSE</b> otherwise.




## -remarks



An <b>EnumUILanguagesProc</b> function can carry out any task. The application registers this function by passing its address to the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a> function.

If MUI_LANGUAGE_ID was specified in the call to <b>EnumUILanguages</b>, the language strings passed to this function will be hexadecimal language 

identifiers that do not include the leading 0x, and will be 4 characters in length. For example, en-US will 

be passed as "0409" and en as "0009".

<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
delegate System.Boolean EnumUILanguagesProc(
            System.IntPtr lpUILanguageString,
            System.IntPtr lParam
            );

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumuilanguagesa">EnumUILanguages</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>
 

 

