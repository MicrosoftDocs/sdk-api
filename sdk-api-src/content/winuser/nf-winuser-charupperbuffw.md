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

# CharUpperBuffW function


## -description


Converts lowercase characters in a buffer to uppercase characters. The function converts the characters in place. 


## -parameters




### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A buffer containing one or more characters to be processed.


### -param cchLength [in]

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <i>lpsz</i>.

The function examines each character, and converts lowercase characters to uppercase characters. The function examines the number of characters indicated by 
					<i>cchLength</i>, even if one or more characters are null characters. 


## -returns



Type: <b>DWORD</b>

The return value is the number of 
						characters processed.

For example, if <b>CharUpperBuff</b>("Zenith of API Sets", 10) succeeds, the return value is 10.




## -remarks



Note that <b>CharUpperBuff</b> always maps lowercase I ("i") to uppercase I, even when the current language is Turkish or Azerbaijani. If you need a function that is linguistically sensitive in this respect, call <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a>.

Conversion to Unicode in the ANSI version of the function is done with the system default locale in all cases.


#### Examples

For an example, see <a href="_win32_Creating_and_Using_a_Temporary_File">Creating and Using a Temporary File</a>. 



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b67786aa-d629-4d23-b4cb-efb43282ca02">CharLower</a>



<a href="https://msdn.microsoft.com/3a678c1b-76a5-4a08-8a13-dfc400492bba">CharLowerBuff</a>



<a href="https://msdn.microsoft.com/4a101fb6-8b90-479b-93dc-3f768e9b952a">CharUpper</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>
 

 

