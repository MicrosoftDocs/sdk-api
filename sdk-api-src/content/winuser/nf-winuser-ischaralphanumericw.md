---
UID: NF:winuser.IsCharAlphaNumericW
title: IsCharAlphaNumericW function
author: windows-sdk-content
description: Determines whether a character is either an alphabetical or a numeric character. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.
old-location: menurc\ischaralphanumeric.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischaralphanumeric.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IsCharAlphaNumeric, IsCharAlphaNumeric function [Menus and Other Resources], IsCharAlphaNumericA, IsCharAlphaNumericW, _win32_IsCharAlphaNumeric, _win32_ischaralphanumeric_cpp, menurc.ischaralphanumeric, winui._win32_ischaralphanumeric, winuser/IsCharAlphaNumeric, winuser/IsCharAlphaNumericA, winuser/IsCharAlphaNumericW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

If the character is not alphanumeric, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/747dd0e0-2d7c-427b-807f-9d0c2de20589">IsCharAlpha</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f2cb0888-b245-448c-9910-a634312aff67">Strings</a>
 

 

