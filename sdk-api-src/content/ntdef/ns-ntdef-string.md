---
UID: NS:ntdef._STRING
title: STRING (ntdef.h)
author: windows-sdk-content
description: The ANSI_STRING structure defines a counted string used for ANSI strings.
old-location: kernel\ansi_string.htm
tech.root: Kernel
ms.assetid: 80bd569a-ed6f-4227-9d14-c011623678a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSTRING, ANSI_STRING, ANSI_STRING structure [Kernel-Mode Driver Architecture], CANSI_STRING, OEM_STRING, PANSI_STRING, PANSI_STRING structure pointer [Kernel-Mode Driver Architecture], STRING, kernel.ansi_string, kstruct_a_0b84d0be-6b91-48b6-87cf-2fd99f043bc4.xml, ntdef/ANSI_STRING, ntdef/PANSI_STRING"
ms.topic: struct
req.header: ntdef.h
req.include-header: Wdm.h, Ntddk.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdef.h
api_name:
 - ANSI_STRING
product: Windows
targetos: Windows
req.typenames: STRING
req.redist: 
---

# STRING structure


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



The <b>ANSI_STRING</b> structure is used to pass ANSI strings. Use the <a href="https://msdn.microsoft.com/7b535ea0-091f-4a1b-bfb7-db3cfabbe846">RtlInitAnsiString</a> routine to initialize an <b>ANSI_STRING</b>.

If the string is null-terminated, <b>Length</b> does not include the terminating <b>NULL</b>.

The <b>MaximumLength</b> is used to indicate the length of <b>Buffer</b> so that if the string is passed to a conversion routine such as <a href="https://msdn.microsoft.com/d05b366c-0b09-4a82-8727-e5c39b82bf7f">RtlUnicodeStringToAnsiString</a> the returned string does not exceed the buffer size.




## -see-also




<a href="https://msdn.microsoft.com/d515eb27-3b18-4b0a-8190-ef15e673bbb7">OEM_STRING</a>



<a href="https://msdn.microsoft.com/32687aa7-4e14-40cb-baa3-4a97d834bf86">RtlAnsiStringToUnicodeSize</a>



<a href="https://msdn.microsoft.com/926d8919-42de-4e24-a223-ffbf412edf6d">RtlAnsiStringToUnicodeString</a>



<a href="https://msdn.microsoft.com/ca46be9e-31f6-4118-8958-4eb2c8450e8c">RtlFreeAnsiString</a>



<a href="https://msdn.microsoft.com/7b535ea0-091f-4a1b-bfb7-db3cfabbe846">RtlInitAnsiString</a>



<a href="https://msdn.microsoft.com/4deaa42e-8c8b-461a-845e-424b543b52b1">RtlUnicodeStringToAnsiSize</a>



<a href="https://msdn.microsoft.com/d05b366c-0b09-4a82-8727-e5c39b82bf7f">RtlUnicodeStringToAnsiString</a>



<a href="https://msdn.microsoft.com/b02f29a9-1049-4e29-aac3-72bf0c70a21e">UNICODE_STRING</a>
 

 

