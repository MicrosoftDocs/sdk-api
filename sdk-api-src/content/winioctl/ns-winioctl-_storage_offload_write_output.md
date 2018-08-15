---
UID: NS:winioctl._STORAGE_OFFLOAD_WRITE_OUTPUT
title: "_STORAGE_OFFLOAD_WRITE_OUTPUT"
author: windows-sdk-content
description: Output structure for the DeviceDsmAction_OffloadWrite action of the IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES control code.
old-location: base\storage_offload_write_output.htm
old-project: devio
ms.assetid: 9da3ac28-93fd-45b7-9ebe-1436593bf591
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PSTORAGE_OFFLOAD_WRITE_OUTPUT, PSTORAGE_OFFLOAD_WRITE_OUTPUT, PSTORAGE_OFFLOAD_WRITE_OUTPUT structure pointer, STORAGE_OFFLOAD_TOKEN_INVALID, STORAGE_OFFLOAD_WRITE_OUTPUT, STORAGE_OFFLOAD_WRITE_OUTPUT structure, STORAGE_OFFLOAD_WRITE_RANGE_TRUNCATED, _STORAGE_OFFLOAD_WRITE_OUTPUT, base.storage_offload_write_output, winioctl/PSTORAGE_OFFLOAD_WRITE_OUTPUT, winioctl/STORAGE_OFFLOAD_WRITE_OUTPUT"
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
req.typenames: STORAGE_OFFLOAD_WRITE_OUTPUT, *PSTORAGE_OFFLOAD_WRITE_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_OFFLOAD_WRITE_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_OFFLOAD_WRITE_OUTPUT structure


## -description


Output structure for the <b>DeviceDsmAction_OffloadWrite</b> action of the 
     <a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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




<a href="https://msdn.microsoft.com/a3f03509-8be9-4cb4-b942-f5ab358bd70e">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/48e797ec-dad2-4a9e-9ccd-aaa65ece8da4">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>
 

 

