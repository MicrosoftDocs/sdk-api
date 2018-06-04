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

# _FILE_STORAGE_TIER structure


## -description


Represents an identifier for the storage tier relative to the volume.


## -struct-fields




### -field Id

Tier ID.


### -field Name

Name for the tier.


### -field Description

Note for the tier.


### -field Flags

The file storage tier flags. This member can be one or more of the following values.

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
 


### -field ProvisionedCapacity

Provisioned capacity of the tier.


### -field MediaType

Media type of the tier.


### -field Class

 




## -remarks



The storage tier ID for a particular volume has no relationship to the storage tier ID with the same value on a different volume.



