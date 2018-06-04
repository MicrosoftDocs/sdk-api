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

# _VIRTUAL_STORAGE_TYPE structure


## -description


Contains the type and provider (vendor) of the virtual storage device.


## -struct-fields




### -field DeviceId

Device type identifier.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VIRTUAL_STORAGE_TYPE_DEVICE_UNKNOWN"></a><a id="virtual_storage_type_device_unknown"></a><dl>
<dt><b>VIRTUAL_STORAGE_TYPE_DEVICE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Device type is unknown or not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="VIRTUAL_STORAGE_TYPE_DEVICE_ISO"></a><a id="virtual_storage_type_device_iso"></a><dl>
<dt><b>VIRTUAL_STORAGE_TYPE_DEVICE_ISO</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
CD or DVD image file device type. (.iso file)

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="VIRTUAL_STORAGE_TYPE_DEVICE_VHD"></a><a id="virtual_storage_type_device_vhd"></a><dl>
<dt><b>VIRTUAL_STORAGE_TYPE_DEVICE_VHD</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Virtual hard disk device type. (.vhd file)

</td>
</tr>
<tr>
<td width="40%"><a id="VIRTUAL_STORAGE_TYPE_DEVICE_VHDX"></a><a id="virtual_storage_type_device_vhdx"></a><dl>
<dt><b>VIRTUAL_STORAGE_TYPE_DEVICE_VHDX</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
VHDX format virtual hard disk device type. (.vhdx file)

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


### -field VendorId

Vendor-unique identifier.



#### VIRTUAL_STORAGE_TYPE_VENDOR_MICROSOFT (EC984AEC-A0F9-47e9-901F-71415A66345B)



#### VIRTUAL_STORAGE_TYPE_VENDOR_UNKNOWN (0)


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">IVdsVdProvider::CreateVDisk</a>



<a href="https://msdn.microsoft.com/e4cdab29-2bb7-4754-9ac8-d6f088910b0d">VDS_VDISK_PROPERTIES</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

