---
UID: NS:ntdef._STRING
title: STRING (ntdef.h)
description: The ANSI_STRING structure defines a counted string used for ANSI strings.helpviewer_keywords: ["*PSTRING","ANSI_STRING","ANSI_STRING structure [Kernel-Mode Driver Architecture]","CANSI_STRING","OEM_STRING","PANSI_STRING","PANSI_STRING structure pointer [Kernel-Mode Driver Architecture]","STRING","kernel.ansi_string","kstruct_a_0b84d0be-6b91-48b6-87cf-2fd99f043bc4.xml","ntdef/ANSI_STRING","ntdef/PANSI_STRING"]
old-location: kernel\ansi_string.htm
tech.root: Kernel
ms.assetid: 80bd569a-ed6f-4227-9d14-c011623678a0
ms.date: 12/05/2018
ms.keywords: '*PSTRING, ANSI_STRING, ANSI_STRING structure [Kernel-Mode Driver Architecture], CANSI_STRING, OEM_STRING, PANSI_STRING, PANSI_STRING structure pointer [Kernel-Mode Driver Architecture], STRING, kernel.ansi_string, kstruct_a_0b84d0be-6b91-48b6-87cf-2fd99f043bc4.xml, ntdef/ANSI_STRING, ntdef/PANSI_STRING'
f1_keywords:
- ntdef/ANSI_STRING
dev_langs:
- c++
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
targetos: Windows
req.typenames: STRING
req.redist: 
ms.custom: 19H1
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



The <b>ANSI_STRING</b> structure is used to pass ANSI strings. Use the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlinitansistring">RtlInitAnsiString</a> routine to initialize an <b>ANSI_STRING</b>.

If the string is null-terminated, <b>Length</b> does not include the terminating <b>NULL</b>.

The <b>MaximumLength</b> is used to indicate the length of <b>Buffer</b> so that if the string is passed to a conversion routine such as <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a> the returned string does not exceed the buffer size.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff558741(v=vs.85)">OEM_STRING</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlansistringtounicodesize">RtlAnsiStringToUnicodeSize</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlansistringtounicodestring">RtlAnsiStringToUnicodeString</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlfreeansistring">RtlFreeAnsiString</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlinitansistring">RtlInitAnsiString</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlunicodestringtoansisize">RtlUnicodeStringToAnsiSize</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/wdm/nf-wdm-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>



[UNICODE_STRING](/windows/win32/api/ntdef/ns-ntdef-_unicode_string)a>
 

 

