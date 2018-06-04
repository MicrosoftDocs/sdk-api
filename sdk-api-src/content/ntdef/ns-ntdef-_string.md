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

# _STRING structure


## -description


The <b>ANSI_STRING</b> structure defines a counted string used for ANSI strings.


## -struct-fields




### -field Length

The length in bytes of the string stored in the buffer pointed to by <b>Buffer</b>.


### -field MaximumLength

The length in bytes of the buffer pointed to by <b>Buffer</b>. 


### -field Buffer

Pointer to a buffer used to contain a string of characters.


### -field Buffer.size_is

 


### -field Buffer.size_is.MaximumLength

 


### -field Buffer.length_is

 


### -field Buffer.length_is.Length

 




## -remarks



The <b>ANSI_STRING</b> structure is used to pass ANSI strings. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff561918">RtlInitAnsiString</a> routine to initialize an <b>ANSI_STRING</b>.

If the string is null-terminated, <b>Length</b> does not include the terminating <b>NULL</b>.

The <b>MaximumLength</b> is used to indicate the length of <b>Buffer</b> so that if the string is passed to a conversion routine such as <a href="https://msdn.microsoft.com/library/windows/hardware/ff562969">RtlUnicodeStringToAnsiString</a> the returned string does not exceed the buffer size.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff558741">OEM_STRING</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561725">RtlAnsiStringToUnicodeSize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561729">RtlAnsiStringToUnicodeString</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561899">RtlFreeAnsiString</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561918">RtlInitAnsiString</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553248">RtlUnicodeStringToAnsiSize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562969">RtlUnicodeStringToAnsiString</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a>
 

 

