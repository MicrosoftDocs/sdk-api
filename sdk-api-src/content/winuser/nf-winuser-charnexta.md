---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CharNextA function


## -description


Retrieves a pointer to the next character in a string. This function can handle strings consisting of either single- or multi-byte characters.


## -parameters




### -param lpsz [in]

Type: <b>LPCTSTR</b>

A character in a null-terminated string.


## -returns



Type: <b>LPTSTR</b>

The return value is a pointer to the next character in the string, or to the terminating null character if at the end of the string.

If 
						<i>lpsz</i> points to the terminating null character, the return value is equal to 
						<i>lpsz</i>.




## -remarks



When called as an ANSI function, <b>CharNext</b> uses the system default code-page, whereas <a href="https://msdn.microsoft.com/0501744a-83a5-4ac4-b934-3e794fe940c0">CharNextExA</a> specifies a code-page to use.


			This function works with default "user" expectations of characters when dealing with diacritics. For example:
A string that contains U+0061 U+030a "LATIN SMALL LETTER A" + COMBINING RING ABOVE" — which looks like "å", will advance two code points, not one.
A string that contains U+0061 U+0301 U+0302 U+0303 U+0304 — which looks like "a´^~¯", will advance five code points, not one,
and so on.
			




## -see-also




<a href="https://msdn.microsoft.com/0501744a-83a5-4ac4-b934-3e794fe940c0">CharNextExA</a>



<a href="https://msdn.microsoft.com/f1599f24-2a6f-4887-8712-302631fee313">CharPrev</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

