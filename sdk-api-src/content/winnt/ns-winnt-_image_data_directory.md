---
UID: NS:winnt._IMAGE_DATA_DIRECTORY
title: "_IMAGE_DATA_DIRECTORY"
author: windows-sdk-content
description: Represents the data directory.
old-location: base\image_data_directory_str.htm
old-project: debug
ms.assetid: 06d53806-d3a3-4990-bc9a-3a3004e60a3c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PIMAGE_DATA_DIRECTORY, IMAGE_DATA_DIRECTORY, IMAGE_DATA_DIRECTORY structure, PIMAGE_DATA_DIRECTORY, PIMAGE_DATA_DIRECTORY structure pointer, _IMAGE_DATA_DIRECTORY, _win32_image_data_directory_str, base.image_data_directory_str, winnt/IMAGE_DATA_DIRECTORY, winnt/PIMAGE_DATA_DIRECTORY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IMAGE_DATA_DIRECTORY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _IMAGE_DATA_DIRECTORY structure


## -description


Represents the data directory.


## -struct-fields




### -field VirtualAddress

The relative virtual address of the table.


### -field Size

The size of the table, in bytes.


## -remarks



The following is a list of the data directories. Offsets are relative to the beginning of the optional header.

<table>
<tr>
<th>Offset (PE/PE32+)</th>
<th>Description</th>
</tr>
<tr>
<td>96/112</td>
<td>Export table address and size</td>
</tr>
<tr>
<td>104/120</td>
<td>Import table address and size</td>
</tr>
<tr>
<td>112/128</td>
<td>Resource table address and size</td>
</tr>
<tr>
<td>120/136</td>
<td>Exception table address and size</td>
</tr>
<tr>
<td>128/144</td>
<td>Certificate table address and size</td>
</tr>
<tr>
<td>136/152</td>
<td>Base relocation table address and size</td>
</tr>
<tr>
<td>144/160</td>
<td>Debugging information starting address and size</td>
</tr>
<tr>
<td>152/168</td>
<td>Architecture-specific data address and size</td>
</tr>
<tr>
<td>160/176</td>
<td>Global pointer register relative virtual address</td>
</tr>
<tr>
<td>168/184</td>
<td>Thread local storage (TLS) table address and size</td>
</tr>
<tr>
<td>176/192</td>
<td>Load configuration table address and size</td>
</tr>
<tr>
<td>184/200</td>
<td>Bound import table address and size</td>
</tr>
<tr>
<td>192/208</td>
<td>Import address table address and size</td>
</tr>
<tr>
<td>200/216</td>
<td>Delay import descriptor address and size</td>
</tr>
<tr>
<td>208/224</td>
<td>The CLR header address and size</td>
</tr>
<tr>
<td>216/232</td>
<td>Reserved</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b6a50ffc-49f8-4824-9b51-7e381eaf8852">IMAGE_OPTIONAL_HEADER</a>



<a href="https://msdn.microsoft.com/b88c7a21-933f-450c-97e8-04cf3c5f9b11">ImageHlp Structures</a>
 

 

