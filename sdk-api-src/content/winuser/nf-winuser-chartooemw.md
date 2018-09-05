---
UID: NF:winuser.CharToOemW
title: CharToOemW function
author: windows-sdk-content
description: Translates a string into the OEM-defined character set.Warning  Do not use.
old-location: menurc\chartooem.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\chartooem.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CharToOem, CharToOem function [Menus and Other Resources], CharToOemA, CharToOemW, _win32_CharToOem, _win32_chartooem_cpp, menurc.chartooem, winui._win32_chartooem, winuser/CharToOem, winuser/CharToOemA, winuser/CharToOemW
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
req.unicode-ansi: CharToOemW (Unicode) and CharToOemA (ANSI)
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
 - Ext-MS-Win-NTUser-chartranslation-l1-1-0.dll
api_name:
 - CharToOem
 - CharToOemA
 - CharToOemW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CharToOemW function


## -description


Translates a string into the OEM-defined character set.
<div class="alert"><b>Warning</b>  Do not use. See Security Considerations.</div><div> </div>

## -parameters




### -param pSrc [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be translated.


### -param pDst [out]

Type: <b>LPSTR</b>

The destination buffer, which receives the translated string. If the <b>CharToOem</b> function is being used as an ANSI function, the string can be translated in place by setting the 
					<i>lpszDst</i> parameter to the same address as the 
					<i>lpszSrc</i> parameter. This cannot be done if <b>CharToOem</b> is being used as a wide-character function. 


## -returns



Type: <b>BOOL</b>

The return value is always nonzero except when you pass the same address to 
						<i>lpszSrc</i> and 
						<i>lpszDst</i> in the wide-character version of the function. In this case the function returns zero and 
						<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_ADDRESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/5b9a968f-c325-48a1-bcc8-79aa5f286bdf">CharToOemBuff</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2336b758-7b57-44d2-b3ce-34054128a26d">OemToChar</a>



<a href="https://msdn.microsoft.com/17b01f13-6c09-43e2-984c-3b085f6b353f">OemToCharBuff</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f2cb0888-b245-448c-9910-a634312aff67">Strings</a>
 

 

