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

# _CSV_NAMESPACE_INFO structure


## -description


Contains the output for the <a href="https://msdn.microsoft.com/E2AB8999-7EF5-4F57-BCFB-79FBECE2E998">FSCTL_IS_CSV_FILE</a> 
    control code that retrieves namespace information for a file.


## -struct-fields




### -field Version

The version number. This value must be set to <b>CSV_NAMESPACE_INFO_V1</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSV_NAMESPACE_INFO_V1"></a><a id="csv_namespace_info_v1"></a><dl>
<dt><b>CSV_NAMESPACE_INFO_V1</b></dt>
</dl>
</td>
<td width="60%">
Version 1.

</td>
</tr>
</table>
 


### -field DeviceNumber

The device number of the disk.


### -field StartingOffset

The starting offset of the volume.


### -field SectorSize

The sector size of the disk.


## -see-also




<a href="https://msdn.microsoft.com/E2AB8999-7EF5-4F57-BCFB-79FBECE2E998">FSCTL_IS_CSV_FILE</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

