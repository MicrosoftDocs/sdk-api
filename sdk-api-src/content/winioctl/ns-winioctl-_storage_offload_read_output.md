---
UID: NS:winioctl._STORAGE_OFFLOAD_READ_OUTPUT
title: "_STORAGE_OFFLOAD_READ_OUTPUT"
author: windows-sdk-content
description: Output structure for the DeviceDsmAction_OffloadRead action of the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
old-location: base\storage_offload_read_output.htm
old-project: devio
ms.assetid: 93eaa8dd-b244-4fdd-abd4-c7cab46cb2a6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PSTORAGE_OFFLOAD_READ_OUTPUT, PSTORAGE_OFFLOAD_READ_OUTPUT, PSTORAGE_OFFLOAD_READ_OUTPUT structure pointer, STORAGE_OFFLOAD_READ_OUTPUT, STORAGE_OFFLOAD_READ_OUTPUT structure, STORAGE_OFFLOAD_READ_RANGE_TRUNCATED, _STORAGE_OFFLOAD_READ_OUTPUT, base.storage_offload_read_output, winioctl/PSTORAGE_OFFLOAD_READ_OUTPUT, winioctl/STORAGE_OFFLOAD_READ_OUTPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: STORAGE_OFFLOAD_READ_OUTPUT, *PSTORAGE_OFFLOAD_READ_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_OFFLOAD_READ_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_OFFLOAD_READ_OUTPUT structure


## -description


Output structure for the <b>DeviceDsmAction_OffloadRead</b> action of the 
     <a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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
        <a href="https://msdn.microsoft.com/5eea412e-ea16-4f47-ac69-46b543069eae">DEVICE_DATA_SET_RANGE</a> structures passed in the 
        <a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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

A <a href="https://msdn.microsoft.com/e33550d6-8d98-4fbb-8e61-d309f0e8e867">STORAGE_OFFLOAD_TOKEN</a> containing the 
      token created.


## -see-also




<a href="https://msdn.microsoft.com/20dd3e5b-90f4-45fc-8cc8-bf9e6d08a026">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>



<a href="https://msdn.microsoft.com/a3f03509-8be9-4cb4-b942-f5ab358bd70e">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/e33550d6-8d98-4fbb-8e61-d309f0e8e867">STORAGE_OFFLOAD_TOKEN</a>
 

 

