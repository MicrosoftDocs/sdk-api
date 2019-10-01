---
UID: NF:winuser.IsCharAlphaNumericW
title: IsCharAlphaNumericW function (winuser.h)
author: windows-sdk-content
description: Determines whether a character is either an alphabetical or a numeric character. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.
old-location: menurc\ischaralphanumeric.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischaralphanumeric.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsCharAlphaNumeric, IsCharAlphaNumeric function [Menus and Other Resources], IsCharAlphaNumericA, IsCharAlphaNumericW, _win32_IsCharAlphaNumeric, _win32_ischaralphanumeric_cpp, menurc.ischaralphanumeric, winui._win32_ischaralphanumeric, winuser/IsCharAlphaNumeric, winuser/IsCharAlphaNumericA, winuser/IsCharAlphaNumericW
ms.topic: function
f1_keywords: 
 - "winuser/IsCharAlphaNumeric"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsCharAlphaNumericW (Unicode) and IsCharAlphaNumericA (ANSI)
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
 - IsCharAlphaNumeric
 - IsCharAlphaNumericA
 - IsCharAlphaNumericW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsCharAlphaNumericW function


## -description


Determines whether a character is either an alphabetical or a numeric character. This determination is based on the semantics of the language selected by the user during setup or through Control Panel. 


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be tested.


## -returns



Type: <b>BOOL</b>

If the character is alphanumeric, the return value is nonzero.

If the character is not alphanumeric, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-ischaralphaa">IsCharAlpha</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/strings">Strings</a>
 

 

