---
UID: NS:winioctl._STORAGE_OFFLOAD_READ_OUTPUT
title: STORAGE_OFFLOAD_READ_OUTPUT
description: Output structure for the DeviceDsmAction_OffloadRead action of the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
helpviewer_keywords: ["*PSTORAGE_OFFLOAD_READ_OUTPUT","PSTORAGE_OFFLOAD_READ_OUTPUT","PSTORAGE_OFFLOAD_READ_OUTPUT structure pointer","STORAGE_OFFLOAD_READ_OUTPUT","STORAGE_OFFLOAD_READ_OUTPUT structure","STORAGE_OFFLOAD_READ_RANGE_TRUNCATED","base.storage_offload_read_output","winioctl/PSTORAGE_OFFLOAD_READ_OUTPUT","winioctl/STORAGE_OFFLOAD_READ_OUTPUT"]
old-location: base\storage_offload_read_output.htm
tech.root: base
ms.assetid: 93eaa8dd-b244-4fdd-abd4-c7cab46cb2a6
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_OFFLOAD_READ_OUTPUT, PSTORAGE_OFFLOAD_READ_OUTPUT, PSTORAGE_OFFLOAD_READ_OUTPUT structure pointer, STORAGE_OFFLOAD_READ_OUTPUT, STORAGE_OFFLOAD_READ_OUTPUT structure, STORAGE_OFFLOAD_READ_RANGE_TRUNCATED, base.storage_offload_read_output, winioctl/PSTORAGE_OFFLOAD_READ_OUTPUT, winioctl/STORAGE_OFFLOAD_READ_OUTPUT'
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
req.typenames: STORAGE_OFFLOAD_READ_OUTPUT, *PSTORAGE_OFFLOAD_READ_OUTPUT
req.redist: 
f1_keywords:
 - _STORAGE_OFFLOAD_READ_OUTPUT
 - winioctl/_STORAGE_OFFLOAD_READ_OUTPUT
 - PSTORAGE_OFFLOAD_READ_OUTPUT
 - winioctl/PSTORAGE_OFFLOAD_READ_OUTPUT
 - STORAGE_OFFLOAD_READ_OUTPUT
 - winioctl/STORAGE_OFFLOAD_READ_OUTPUT
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
 - STORAGE_OFFLOAD_READ_OUTPUT
---

# STORAGE_OFFLOAD_READ_OUTPUT structure


## -description

Output structure for the <b>DeviceDsmAction_OffloadRead</b> action of the 
     <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     control code.

## -struct-fields

### -field OffloadReadFlags

Output flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STORAGE_OFFLOAD_READ_RANGE_TRUNCATED"></a><a id="storage_offload_read_range_truncated"></a><dl>
<dt><b>STORAGE_OFFLOAD_READ_RANGE_TRUNCATED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The ranges represented by the token is smaller than the ranges specified in the 
        <a href="/windows/desktop/api/winioctl/ns-winioctl-device_data_set_range">DEVICE_DATA_SET_RANGE</a> structures passed in the 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
        control code input buffer. In other words the <b>LengthProtected</b> member is less than 
        the sum of all of the <b>LengthInBytes</b> members of the 
        <b>DEVICE_DATA_SET_RANGE</b> structures passed.

</td>
</tr>
</table>

### -field Reserved

Reserved.

### -field LengthProtected

The total length of the snapshot represented by the token.

### -field TokenLength

Length of the token in bytes.

### -field Token

A <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_token">STORAGE_OFFLOAD_TOKEN</a> containing the 
      token created.

## -see-also

<a href="/windows/win32/api/winioctl/ns-winioctl-device_dsm_offload_read_parameters">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-device_manage_data_set_attributes_output">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_manage_data_set_attributes">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_offload_token">STORAGE_OFFLOAD_TOKEN</a>