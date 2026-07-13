---
UID: NS:winioctl._GET_DISK_ATTRIBUTES
title: GET_DISK_ATTRIBUTES
description: Contains the attributes of a disk device.
helpviewer_keywords: ["*PGET_DISK_ATTRIBUTES","DISK_ATTRIBUTE_OFFLINE","DISK_ATTRIBUTE_READ_ONLY","GET_DISK_ATTRIBUTES","GET_DISK_ATTRIBUTES structure [Files]","PGET_DISK_ATTRIBUTES","PGET_DISK_ATTRIBUTES structure pointer [Files]","fs.get_disk_attributes","winioctl/GET_DISK_ATTRIBUTES","winioctl/PGET_DISK_ATTRIBUTES"]
old-location: fs\get_disk_attributes.htm
tech.root: fs
ms.assetid: c6a0461d-cc23-4191-a0ff-c4279c1b097e
ms.date: 12/05/2018
ms.keywords: '*PGET_DISK_ATTRIBUTES, DISK_ATTRIBUTE_OFFLINE, DISK_ATTRIBUTE_READ_ONLY, GET_DISK_ATTRIBUTES, GET_DISK_ATTRIBUTES structure [Files], PGET_DISK_ATTRIBUTES, PGET_DISK_ATTRIBUTES structure pointer [Files], fs.get_disk_attributes, winioctl/GET_DISK_ATTRIBUTES, winioctl/PGET_DISK_ATTRIBUTES'
req.header: winioctl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GET_DISK_ATTRIBUTES, *PGET_DISK_ATTRIBUTES
req.redist: 
f1_keywords:
 - _GET_DISK_ATTRIBUTES
 - winioctl/_GET_DISK_ATTRIBUTES
 - PGET_DISK_ATTRIBUTES
 - winioctl/PGET_DISK_ATTRIBUTES
 - GET_DISK_ATTRIBUTES
 - winioctl/GET_DISK_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - GET_DISK_ATTRIBUTES
---

# GET_DISK_ATTRIBUTES structure


## -description

Contains the attributes of a disk device. Returned as the output buffer from the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_disk_attributes">IOCTL_DISK_GET_DISK_ATTRIBUTES</a> control 
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

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_disk_attributes">IOCTL_DISK_GET_DISK_ATTRIBUTES</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-set_disk_attributes">SET_DISK_ATTRIBUTES</a>