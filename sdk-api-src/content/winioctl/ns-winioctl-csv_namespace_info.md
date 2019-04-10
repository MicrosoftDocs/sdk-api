---
UID: NS:winioctl._CSV_NAMESPACE_INFO
title: CSV_NAMESPACE_INFO (winioctl.h)
author: windows-sdk-content
description: Contains the output for the FSCTL_IS_CSV_FILE control code that retrieves namespace information for a file.
old-location: fs\csv_namespace_info.htm
tech.root: FileIO
ms.assetid: E6F3D334-6974-40E2-B00A-17CA5F05C3F4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCSV_NAMESPACE_INFO, CSV_NAMESPACE_INFO, CSV_NAMESPACE_INFO structure [Files], CSV_NAMESPACE_INFO_V1, PCSV_NAMESPACE_INFO, PCSV_NAMESPACE_INFO structure pointer [Files], fs.csv_namespace_info, winioctl/CSV_NAMESPACE_INFO, winioctl/PCSV_NAMESPACE_INFO"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - WinIoCtl.h
api_name:
 - CSV_NAMESPACE_INFO
product: Windows
targetos: Windows
req.typenames: CSV_NAMESPACE_INFO, *PCSV_NAMESPACE_INFO
req.redist: 
---

# CSV_NAMESPACE_INFO structure


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
 

 

