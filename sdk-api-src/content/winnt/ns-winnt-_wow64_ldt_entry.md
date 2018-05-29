---
UID: NS:winnt._WOW64_LDT_ENTRY
title: "_WOW64_LDT_ENTRY"
author: windows-sdk-content
description: Describes an entry in the descriptor table for a 32-bit thread on a 64-bit system. This structure is valid only on 64-bit systems.
old-location: base\wow64_ldt_entry_str.htm
old-project: Debug
ms.assetid: a571cd2f-0873-4ad5-bcb8-c0da2d47a820
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PWOW64_LDT_ENTRY, PWOW64_LDT_ENTRY, PWOW64_LDT_ENTRY structure pointer, WOW64_LDT_ENTRY, WOW64_LDT_ENTRY structure, _WOW64_LDT_ENTRY, base.wow64_ldt_entry_str, winnt/LDT_ENTRY, winnt/PWOW64_LDT_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WOW64_LDT_ENTRY, *PWOW64_LDT_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	WOW64_LDT_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WOW64_LDT_ENTRY structure


## -description


Describes an entry in the descriptor table for a 32-bit thread on a 64-bit system. This structure is valid only on 64-bit systems.


## -struct-fields




### -field LimitLow

The low-order part of the address of the last byte in the segment.


### -field BaseLow

The low-order part of the base address of the segment.


### -field HighWord

The high-order portion of the descriptor. This member may be interpreted as bytes or collections of bits, depending on the level of detail required. 



					


### -field HighWord.Bytes


### -field HighWord.Bytes.BaseMid

Middle bits (16â€“23) of the base address of the segment.


### -field HighWord.Bytes.Flags1

Values of the <b>Type</b>, <b>Dpl</b>, and <b>Pres</b> members in the <b>Bits</b> structure.


### -field HighWord.Bytes.Flags2

Values of the <b>LimitHi</b>, <b>Sys</b>, <b>Reserved_0</b>, <b>Default_Big</b>, and <b>Granularity</b> members in the <b>Bits</b> structure.


### -field HighWord.Bytes.BaseHi

High bits (24â€“31) of the base address of the segment.


### -field HighWord.Bits


### -field HighWord.Bits.BaseMid

The middle bits (16â€“23) of the base address of the segment.


### -field HighWord.Bits.Type

The type of segment. This member can be one of the following values:


### -field HighWord.Bits.Dpl

The privilege level of the descriptor. This member is an integer value in the range 0 (most privileged) through 3 (least privileged).


### -field HighWord.Bits.Pres

The present flag. This member is 1 if the segment is present in physical memory or 0 if it is not.


### -field HighWord.Bits.LimitHi

The high bits (16â€“19) of the address of the last byte in the segment.


### -field HighWord.Bits.Sys

The space that is available to system programmers. This member might be used for marking segments in some system-specific way.


### -field HighWord.Bits.Reserved_0

Reserved.


### -field HighWord.Bits.Default_Big

The size of segment. If the segment is a data segment, this member contains 1 if the segment is larger than 64 kilobytes (KB) or 0 if the segment is smaller than or equal to 64 KB. 




If the segment is a code segment, this member contains 1. The segment runs with the default (native mode) instruction set. 


### -field HighWord.Bits.Granularity

The granularity. This member contains 0 if the segment is byte granular, 1 if the segment is page granular.


### -field HighWord.Bits.BaseHi

The high bits (24â€“31) of the base address of the segment.


## -remarks



The 
<a href="https://msdn.microsoft.com/68393913-6725-4cc6-90b9-57da2a96c91e">Wow64GetThreadSelectorEntry</a> function fills this structure with information from an entry in the descriptor table. You can use this information to convert a segment-relative address to a linear virtual address.

The base address of a segment is the address of offset 0 in the segment. To calculate this value, combine the <b>BaseLow</b>, <b>BaseMid</b>, and <b>BaseHi</b> members.

The limit of a segment is the address of the last byte that can be addressed in the segment. To calculate this value, combine the <b>LimitLow</b> and <b>LimitHi</b> members.

The <b>WOW64_LDT_ENTRY</b> structure has the same layout for a 64-bit process as the <a href="https://msdn.microsoft.com/e4c470ee-63e5-4a00-8c69-76cadd490439">LDT_ENTRY</a> structure has for a 32-bit process.




## -see-also




<a href="https://msdn.microsoft.com/bf1294cd-1836-49d3-9cc4-4532429a301f">Debugging Structures</a>



<a href="https://msdn.microsoft.com/68393913-6725-4cc6-90b9-57da2a96c91e">Wow64GetThreadSelectorEntry</a>
 

 

