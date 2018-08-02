---
UID: NS:winioctl._FSCTL_QUERY_STORAGE_CLASSES_OUTPUT
title: "_FSCTL_QUERY_STORAGE_CLASSES_OUTPUT"
author: windows-sdk-content
description: Contains information for all tiers of a specific volume.
old-location: fs\fsctl_query_storage_classes_output.htm
old-project: FileIO
ms.assetid: 376B457C-2D54-47D0-A80A-16A03DA6A2EA
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY, FSCTL_QUERY_STORAGE_CLASSES_OUTPUT, FSCTL_QUERY_STORAGE_CLASSES_OUTPUT structure [Files], PFSCTL_QUERY_STORAGE_CLASSES_OUTPUT, PFSCTL_QUERY_STORAGE_CLASSES_OUTPUT structure pointer [Files], _FSCTL_QUERY_STORAGE_CLASSES_OUTPUT, fs.fsctl_query_storage_classes_output, winioctl/FSCTL_QUERY_STORAGE_CLASSES_OUTPUT, winioctl/PFSCTL_QUERY_STORAGE_CLASSES_OUTPUT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: FSCTL_QUERY_STORAGE_CLASSES_OUTPUT, PFSCTL_QUERY_STORAGE_CLASSES_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - FSCTL_QUERY_STORAGE_CLASSES_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FSCTL_QUERY_STORAGE_CLASSES_OUTPUT structure


## -description


Contains information for all tiers of a specific volume.


## -struct-fields




### -field Version

The size of this structure serves as the version.  Set it to <b>sizeof</b>(<b>FSCTL_QUERY_STORAGE_CLASSES_OUTPUT</b>).


### -field Size

Size of this structure plus all the variable sized fields.


### -field Flags

The element status. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY"></a><a id="file_storage_tier_flag_no_seek_penalty"></a><dl>
<dt><b>FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Tier does not suffer a seek penalty on IO operations, which indicates that is an SSD (solid state drive).

</td>
</tr>
</table>
 


### -field TotalNumberOfTiers

Total number of available tiers for this disk.


### -field NumberOfTiersReturned

Number of tiers that fit in the output.


### -field Tiers


<a href="https://msdn.microsoft.com/F9701D3B-57B3-4777-841C-3D45A2CEC17E">FILE_STORAGE_TIER</a> structure that contains detailed info on the storage tiers.

