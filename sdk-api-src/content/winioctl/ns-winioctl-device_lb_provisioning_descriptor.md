---
UID: NS:winioctl._DEVICE_LB_PROVISIONING_DESCRIPTOR
title: DEVICE_LB_PROVISIONING_DESCRIPTOR
author: windows-sdk-content
description: Contains the thin provisioning capabilities for a storage device.
old-location: fs\device_lb_provisioning_descriptor.htm
tech.root: FileIO
ms.assetid: dbc46b33-9e9d-4ccf-9bc9-1df70738fa73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDEVICE_LB_PROVISIONING_DESCRIPTOR, DEVICE_LB_PROVISIONING_DESCRIPTOR, DEVICE_LB_PROVISIONING_DESCRIPTOR structure [Files], PDEVICE_LB_PROVISIONING_DESCRIPTOR, PDEVICE_LB_PROVISIONING_DESCRIPTOR structure pointer [Files], fs.device_lb_provisioning_descriptor, winioctl/DEVICE_LB_PROVISIONING_DESCRIPTOR, winioctl/PDEVICE_LB_PROVISIONING_DESCRIPTOR"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DEVICE_LB_PROVISIONING_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: DEVICE_LB_PROVISIONING_DESCRIPTOR, *PDEVICE_LB_PROVISIONING_DESCRIPTOR
req.redist: 
---

# DEVICE_LB_PROVISIONING_DESCRIPTOR structure


## -description


The 
   <b>DEVICE_LB_PROVISIONING_DESCRIPTOR</b> 
   structure is one of the query result structures returned from an 
   <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This 
   structure contains the thin provisioning capabilities for a storage device.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.


### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.


### -field ThinProvisioningEnabled

The thin provisioning–enabled status.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Thin provisioning is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Thin provisioning is enabled.

</td>
</tr>
</table>
 


### -field ThinProvisioningReadZeros

Reads to unmapped regions return zeros.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Data read from unmapped regions is undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Reads return zeros.

</td>
</tr>
</table>
 


### -field AnchorSupported

Deterministic read after trim support.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Deterministic read after trim is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Deterministic read after trim is supported.

</td>
</tr>
</table>
 


### -field UnmapGranularityAlignmentValid

The validity of unmap granularity alignment for the device.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unmap granularity alignment is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Unmap granularity alignment is valid.

</td>
</tr>
</table>
 


### -field Reserved0

Reserved.


### -field Reserved1

Reserved.


### -field OptimalUnmapGranularity

The optimal number of logical sectors for unmap granularity for the device.


### -field UnmapGranularityAlignment

The current value, in logical sectors, set for unmap granularity alignment on the device.


### -field MaxUnmapLbaCount

<b>Starting in Windows 10: </b>The maximum number of LBAs that can be unmapped in a single unmap command, in logical blocks.


### -field MaxUnmapBlockDescriptorCount

<b>Starting in Windows 10: </b>The maximum number of descriptors allowed in a single unmap command.


## -remarks



This structure is returned from a 
    <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request when the 
    <b>PropertyId</b> member of 
    <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> is set to 
    <b>StorageDeviceLBProvisioningProperty</b>.

If <b>UnmapGranularityAlignmentValid</b> = 0, then any code using 
    <b>UnmapGranularityAlignment</b> should assume it has a value of 0.




## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

