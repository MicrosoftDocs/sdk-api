---
UID: NS:ntdef._UNICODE_STRING
title: _UNICODE_STRING (ntdef.h)
description: The UNICODE_STRING structure is used to define Unicode strings.
old-location: kernel\unicode_string.htm
tech.root: kernel
ms.assetid: b02f29a9-1049-4e29-aac3-72bf0c70a21e
ms.date: 04/30/2018
ms.keywords: "*PUNICODE_STRING, PUNICODE_STRING, PUNICODE_STRING structure pointer [Kernel-Mode Driver Architecture], UNICODE_STRING, UNICODE_STRING structure [Kernel-Mode Driver Architecture], _UNICODE_STRING, kernel.unicode_string, kstruct_d_9f862aaa-4cd6-4420-8255-ad577d8a8c59.xml, ntdef/PUNICODE_STRING, ntdef/UNICODE_STRING"
ms.topic: struct
req.header: ntdef.h
req.include-header: Wdm.h, Ntddk.h, Ntdef.h
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
- ntdef.h
api_name:
- UNICODE_STRING
product:
- Windows
targetos: Windows
req.typenames: UNICODE_STRING
---

# _UNICODE_STRING structure

## -description

The **UNICODE_STRING** structure is used to define Unicode strings.

## -syntax

```
typedef struct _UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING, *PUNICODE_STRING;
```

## -struct-fields

### -field Length

The length, in bytes, of the string stored in **Buffer**.

### -field MaximumLength

The length, in bytes, of **Buffer**.

### -field Buffer

Pointer to a buffer used to contain a string of wide characters.

## -remarks

The **UNICODE_STRING** structure is used to pass Unicode strings. Use [RtlUnicodeStringInit](https://msdn.microsoft.com/library/windows/hardware/ff562954) or [RtlUnicodeStringInitEx](https://msdn.microsoft.com/library/windows/hardware/ff562958) to initialize a **UNICODE_STRING** structure.

If the string is null-terminated, **Length** does not include the trailing null character.

The **MaximumLength** is used to indicate the length of **Buffer** so that if the string is passed to a conversion routine such as [RtlAnsiStringToUnicodeString](https://msdn.microsoft.com/library/windows/hardware/ff561729) the returned string does not exceed the buffer size.

## -see-also

[ANSI_STRING](https://msdn.microsoft.com/library/windows/hardware/ff540605)

[OEM_STRING](https://msdn.microsoft.com/library/windows/hardware/ff558741)

[RtlAnsiStringToUnicodeSize](https://msdn.microsoft.com/library/windows/hardware/ff561725)

[RtlAnsiStringToUnicodeString](https://msdn.microsoft.com/library/windows/hardware/ff561729)

[RtlFreeUnicodeString](https://msdn.microsoft.com/library/windows/hardware/ff561903)

[RtlInitUnicodeString](https://msdn.microsoft.com/library/windows/hardware/ff561934)

[RtlUnicodeStringToAnsiSize](https://msdn.microsoft.com/library/windows/hardware/ff553248)

[RtlUnicodeStringToAnsiString](https://msdn.microsoft.com/library/windows/hardware/ff562969)
