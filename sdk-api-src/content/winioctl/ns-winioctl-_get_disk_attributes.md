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

# _GET_DISK_ATTRIBUTES structure


## -description


Contains the attributes of a disk device. Returned as the output buffer from the 
    <a href="https://msdn.microsoft.com/3fa9fabb-91ef-4306-90b6-c3dd17f3e298">IOCTL_DISK_GET_DISK_ATTRIBUTES</a> control 
    code.


## -struct-fields




### -field Version

Set to <code>sizeof(GET_DISK_ATTRIBUTES)</code>.


### -field Reserved1

Reserved.


### -field Attributes

Contains attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_OFFLINE"></a><a id="disk_attribute_offline"></a><dl>
<dt><b>DISK_ATTRIBUTE_OFFLINE</b></dt>
<dt>0x0000000000000001</dt>
</dl>
</td>
<td width="60%">
The disk is offline.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_READ_ONLY"></a><a id="disk_attribute_read_only"></a><dl>
<dt><b>DISK_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x0000000000000002</dt>
</dl>
</td>
<td width="60%">
The disk is read-only.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/3fa9fabb-91ef-4306-90b6-c3dd17f3e298">IOCTL_DISK_GET_DISK_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/ba0e3666-8660-493c-b821-5997d577e7e2">SET_DISK_ATTRIBUTES</a>
 

 

