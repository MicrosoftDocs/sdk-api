---
UID: NS:minidumpapiset._MINIDUMP_LOCATION_DESCRIPTOR64
title: "_MINIDUMP_LOCATION_DESCRIPTOR64"
author: windows-sdk-content
description: Contains information describing the location of a data stream within a minidump file.
old-location: base\minidump_location_descriptor_str.htm
old-project: debug
ms.assetid: aef17239-9b56-4d49-8347-610270f8612b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MINIDUMP_LOCATION_DESCRIPTOR, MINIDUMP_LOCATION_DESCRIPTOR structure, MINIDUMP_LOCATION_DESCRIPTOR64, _MINIDUMP_LOCATION_DESCRIPTOR, _MINIDUMP_LOCATION_DESCRIPTOR64, _win32_minidump_location_descriptor_str, base.minidump_location_descriptor_str, minidumpapiset/MINIDUMP_LOCATION_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h, Minidumpapiset.h
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
tech.root: 
req.typenames: MINIDUMP_LOCATION_DESCRIPTOR64
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_LOCATION_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_LOCATION_DESCRIPTOR64 structure


## -description


Contains information describing the location of a data stream within a minidump file.


## -struct-fields




### -field DataSize

The size of the data stream, in bytes.


### -field Rva

The relative virtual address (RVA) of the data. This is the byte offset of the data stream from the beginning of the minidump file.


## -remarks



In this context, a data stream refers to a block of data within a minidump file.

This structure uses 32-bit locations for RVAs in the first 4GB and 64-bit locations are used for larger RVAs. The <b>MINIDUMP_LOCATION_DESCRIPTOR64</b> structure is defined as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
typedef struct _MINIDUMP_LOCATION_DESCRIPTOR64 {
  ULONG64 DataSize;
  RVA64 Rva;
} MINIDUMP_LOCATION_DESCRIPTOR64;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a>



<a href="https://msdn.microsoft.com/2de717dc-a9ac-4b81-9fab-992f22da9a0d">MINIDUMP_EXCEPTION_STREAM</a>



<a href="https://msdn.microsoft.com/34c6de99-8ba5-4199-a382-3e3f7d02571f">MINIDUMP_MEMORY_DESCRIPTOR</a>
 

 

