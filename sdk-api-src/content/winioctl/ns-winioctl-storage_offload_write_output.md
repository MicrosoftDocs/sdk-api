---
UID: NS:winioctl._STORAGE_OFFLOAD_WRITE_OUTPUT
title: STORAGE_OFFLOAD_WRITE_OUTPUT
description: Output structure for the DeviceDsmAction_OffloadWrite action of the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PSTORAGE_OFFLOAD_WRITE_OUTPUT","PSTORAGE_OFFLOAD_WRITE_OUTPUT","PSTORAGE_OFFLOAD_WRITE_OUTPUT structure pointer","STORAGE_OFFLOAD_TOKEN_INVALID","STORAGE_OFFLOAD_WRITE_OUTPUT","STORAGE_OFFLOAD_WRITE_OUTPUT structure","STORAGE_OFFLOAD_WRITE_RANGE_TRUNCATED","base.storage_offload_write_output","winioctl/PSTORAGE_OFFLOAD_WRITE_OUTPUT","winioctl/STORAGE_OFFLOAD_WRITE_OUTPUT"]
old-location: base\storage_offload_write_output.htm
tech.root: base
ms.assetid: 9da3ac28-93fd-45b7-9ebe-1436593bf591
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_OFFLOAD_WRITE_OUTPUT, PSTORAGE_OFFLOAD_WRITE_OUTPUT, PSTORAGE_OFFLOAD_WRITE_OUTPUT structure pointer, STORAGE_OFFLOAD_TOKEN_INVALID, STORAGE_OFFLOAD_WRITE_OUTPUT, STORAGE_OFFLOAD_WRITE_OUTPUT structure, STORAGE_OFFLOAD_WRITE_RANGE_TRUNCATED, base.storage_offload_write_output, winioctl/PSTORAGE_OFFLOAD_WRITE_OUTPUT, winioctl/STORAGE_OFFLOAD_WRITE_OUTPUT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: STORAGE_OFFLOAD_WRITE_OUTPUT, *PSTORAGE_OFFLOAD_WRITE_OUTPUT
req.redist: 
f1_keywords:
 - _STORAGE_OFFLOAD_WRITE_OUTPUT
 - winioctl/_STORAGE_OFFLOAD_WRITE_OUTPUT
 - PSTORAGE_OFFLOAD_WRITE_OUTPUT
 - winioctl/PSTORAGE_OFFLOAD_WRITE_OUTPUT
 - STORAGE_OFFLOAD_WRITE_OUTPUT
 - winioctl/STORAGE_OFFLOAD_WRITE_OUTPUT
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
 - STORAGE_OFFLOAD_WRITE_OUTPUT
---

# STORAGE_OFFLOAD_WRITE_OUTPUT structure


## -description

Output structure for the <b>DeviceDsmAction_OffloadWrite</b> action of the 
     <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     control code.

## -struct-fields

### -field OffloadWriteFlags

Out flags

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STORAGE_OFFLOAD_WRITE_RANGE_TRUNCATED"></a><a id="storage_offload_write_range_truncated"></a><dl>
<dt><b>STORAGE_OFFLOAD_WRITE_RANGE_TRUNCATED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The range written is less than the range specified.

</td>
</tr>
<tr>
<td width="40%"><a id="STORAGE_OFFLOAD_TOKEN_INVALID"></a><a id="storage_offload_token_invalid"></a><dl>
<dt><b>STORAGE_OFFLOAD_TOKEN_INVALID</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The token specified is not valid.

</td>
</tr>
</table>

### -field Reserved

Reserved.

### -field LengthCopied

The length of the copied content.

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes_output">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>