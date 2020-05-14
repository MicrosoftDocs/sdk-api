---
UID: NF:winuser.IsCharAlphaA
title: IsCharAlphaA function (winuser.h)
description: Determines whether a character is an alphabetical character. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.helpviewer_keywords: ["IsCharAlpha","IsCharAlpha function [Menus and Other Resources]","IsCharAlphaA","IsCharAlphaW","_win32_IsCharAlpha","_win32_ischaralpha_cpp","menurc.ischaralpha","winui._win32_ischaralpha","winuser/IsCharAlpha","winuser/IsCharAlphaA","winuser/IsCharAlphaW"]
old-location: menurc\ischaralpha.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischaralpha.htm
ms.date: 12/05/2018
ms.keywords: IsCharAlpha, IsCharAlpha function [Menus and Other Resources], IsCharAlphaA, IsCharAlphaW, _win32_IsCharAlpha, _win32_ischaralpha_cpp, menurc.ischaralpha, winui._win32_ischaralpha, winuser/IsCharAlpha, winuser/IsCharAlphaA, winuser/IsCharAlphaW
f1_keywords:
- winuser/IsCharAlpha
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsCharAlphaW (Unicode) and IsCharAlphaA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
- API-MS-Win-Core-String-l2-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-String-l2-1-1.dll
- API-MS-Win-Core-Stringansi-l1-1-0.dll
- API-MS-Win-DownLevel-user32-l1-1-0.dll
- API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
- IsCharAlpha
- IsCharAlphaA
- IsCharAlphaW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsCharAlphaA function


## -description


Determines whether a character is an alphabetical character. This determination is based on the semantics of the language selected by the user during setup or through Control Panel. 


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be tested.


## -returns



Type: <b>BOOL</b>

If the character is alphabetical, the return value is nonzero.

If the character is not alphabetical, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-ischaralphanumerica">IsCharAlphaNumeric</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

 

