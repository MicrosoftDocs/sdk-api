---
UID: NF:winbase.lstrcatW
title: lstrcatW function
author: windows-sdk-content
description: Appends one string to another.Warning  Do not use.
old-location: menurc\lstrcat.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcat.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_lstrcat, _win32_lstrcat_cpp, lstrcat, lstrcat function [Menus and Other Resources], lstrcatA, lstrcatW, menurc.lstrcat, winbase/lstrcat, winbase/lstrcatA, winbase/lstrcatW, winui._win32_lstrcat"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrcatW (Unicode) and lstrcatA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - lstrcat
 - lstrcatA
 - lstrcatW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# lstrcatW function


## -description


Appends one string to another.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="https://msdn.microsoft.com/72ddb6ab-8167-4213-815b-bd15b62d6123">StringCchCat</a> instead. See Security Considerations. </div><div> </div>

## -parameters




### -param lpString1 [in, out]

Type: <b>LPTSTR</b>

The first null-terminated string. This buffer must be large enough 
				to contain both strings.


### -param lpString2 [in]

Type: <b>LPTSTR</b>

The null-terminated string to be appended to the string 
				specified in the <i>lpString1</i> parameter.


## -returns



Type: <b>LPTSTR</b>

If the function succeeds, the return value is a pointer to the buffer.

If the function fails, the return value is <b>NULL</b> 
                    and <i>lpString1</i> may not be null-terminated.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6330483b-dc61-4bbf-8ee7-e91a93495bb2">StringCbCat</a>



<a href="https://msdn.microsoft.com/db9f0731-0f7b-4018-ad07-1abe0bfe71e8">StringCbCatEx</a>



<a href="https://msdn.microsoft.com/56ef4ada-52df-48dd-a5e1-f62311be7592">StringCbCatN</a>



<a href="https://msdn.microsoft.com/ad1cad70-c548-4b2f-b253-b0af5000df08">StringCbCatNEx</a>



<a href="https://msdn.microsoft.com/72ddb6ab-8167-4213-815b-bd15b62d6123">StringCchCat</a>



<a href="https://msdn.microsoft.com/3b829dfa-6ede-47bd-b4d7-fcbf94a26c50">StringCchCatEx</a>



<a href="https://msdn.microsoft.com/516b67f9-ab6e-4c23-b04a-01848de09115">StringCchCatN</a>



<a href="https://msdn.microsoft.com/63c9f437-b769-4c5a-9168-d0c458947abc">StringCchCatNEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>



<a href="https://msdn.microsoft.com/e7b6ac43-ef24-4121-bb4e-a01232b034ad">lstrcmp</a>



<a href="https://msdn.microsoft.com/7edd4896-04d3-4b71-9ce6-d64149d683e0">lstrcmpi</a>



<a href="https://msdn.microsoft.com/0024853f-3a1f-4742-bc5e-f0ca89e23f3a">lstrlen</a>
 

 

