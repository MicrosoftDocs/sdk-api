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

# _STORAGE_OFFLOAD_READ_OUTPUT structure


## -description


Output structure for the <b>DeviceDsmAction_OffloadRead</b> action of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff552523">DEVICE_DATA_SET_RANGE</a> structures passed in the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
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

A <a href="https://msdn.microsoft.com/library/windows/hardware/hh451469">STORAGE_OFFLOAD_TOKEN</a> containing the 
      token created.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439639">DEVICE_DSM_OFFLOAD_READ_PARAMETERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439656">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451469">STORAGE_OFFLOAD_TOKEN</a>
 

 

