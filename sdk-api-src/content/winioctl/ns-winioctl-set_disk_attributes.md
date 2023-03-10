---
UID: NS:winioctl._SET_DISK_ATTRIBUTES
title: SET_DISK_ATTRIBUTES
description: Specifies the attributes to be set on a disk device.
helpviewer_keywords: ["*PSET_DISK_ATTRIBUTES","DISK_ATTRIBUTE_OFFLINE","DISK_ATTRIBUTE_READ_ONLY","PSET_DISK_ATTRIBUTES","PSET_DISK_ATTRIBUTES structure pointer [Files]","SET_DISK_ATTRIBUTES","SET_DISK_ATTRIBUTES structure [Files]","fs.set_disk_attributes","winioctl/PSET_DISK_ATTRIBUTES","winioctl/SET_DISK_ATTRIBUTES"]
old-location: fs\set_disk_attributes.htm
tech.root: fs
ms.assetid: 2caa79aa-24f9-481d-bbe3-ecd3e49bf316
ms.date: 12/05/2018
ms.keywords: '*PSET_DISK_ATTRIBUTES, DISK_ATTRIBUTE_OFFLINE, DISK_ATTRIBUTE_READ_ONLY, PSET_DISK_ATTRIBUTES, PSET_DISK_ATTRIBUTES structure pointer [Files], SET_DISK_ATTRIBUTES, SET_DISK_ATTRIBUTES structure [Files], fs.set_disk_attributes, winioctl/PSET_DISK_ATTRIBUTES, winioctl/SET_DISK_ATTRIBUTES'
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
req.typenames: SET_DISK_ATTRIBUTES, *PSET_DISK_ATTRIBUTES
req.redist: 
f1_keywords:
 - _SET_DISK_ATTRIBUTES
 - winioctl/_SET_DISK_ATTRIBUTES
 - PSET_DISK_ATTRIBUTES
 - winioctl/PSET_DISK_ATTRIBUTES
 - SET_DISK_ATTRIBUTES
 - winioctl/SET_DISK_ATTRIBUTES
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
 - SET_DISK_ATTRIBUTES
---

# SET_DISK_ATTRIBUTES structure


## -description

Specifies the attributes to be set on a disk device. Passed as the input buffer to the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_disk_attributes">IOCTL_DISK_SET_DISK_ATTRIBUTES</a> control 
    code.

## -struct-fields

### -field Version

Set to <code>sizeof(GET_DISK_ATTRIBUTES)</code>.

### -field Persist

If <b>TRUE</b>, these settings are persisted across reboots.

### -field Reserved1

 Reserved. Must be set to <b>FALSE</b> (0).

### -field Attributes

 Specifies attributes.

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

### -field AttributesMask

Indicates which attributes are being changed.

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
The offline attribute is being changed.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_READ_ONLY"></a><a id="disk_attribute_read_only"></a><dl>
<dt><b>DISK_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x0000000000000002</dt>
</dl>
</td>
<td width="60%">
The read-only attribute is being changed.

</td>
</tr>
</table>

### -field Reserved2

Reserved. Must be set to 0.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-get_disk_attributes">GET_DISK_ATTRIBUTES</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_disk_attributes">IOCTL_DISK_SET_DISK_ATTRIBUTES</a>