---
UID: NS:virtdisk._VIRTUAL_STORAGE_TYPE
title: VIRTUAL_STORAGE_TYPE (virtdisk.h)
description: Contains the type and provider (vendor) of the virtual storage device.
helpviewer_keywords: ["*PVIRTUAL_STORAGE_TYPE","PVIRTUAL_STORAGE_TYPE","PVIRTUAL_STORAGE_TYPE structure pointer [VHD]","VIRTUAL_STORAGE_TYPE","VIRTUAL_STORAGE_TYPE structure [VHD]","VIRTUAL_STORAGE_TYPE_DEVICE_ISO","VIRTUAL_STORAGE_TYPE_DEVICE_UNKNOWN","VIRTUAL_STORAGE_TYPE_DEVICE_VHD","VIRTUAL_STORAGE_TYPE_DEVICE_VHDX","VIRTUAL_STORAGE_TYPE_VENDOR_MICROSOFT","VIRTUAL_STORAGE_TYPE_VENDOR_UNKNOWN","_VIRTUAL_STORAGE_TYPE","vdssys/PVIRTUAL_STORAGE_TYPE","vdssys/VIRTUAL_STORAGE_TYPE","vhd.virtual_storage_type","virtdisk/PVIRTUAL_STORAGE_TYPE","virtdisk/VIRTUAL_STORAGE_TYPE"]
old-location: vhd\virtual_storage_type.htm
tech.root: VStor
ms.assetid: 9f0c1848-fa8e-4747-a3b1-71a274695280
ms.date: 12/05/2018
ms.keywords: '*PVIRTUAL_STORAGE_TYPE, PVIRTUAL_STORAGE_TYPE, PVIRTUAL_STORAGE_TYPE structure pointer [VHD], VIRTUAL_STORAGE_TYPE, VIRTUAL_STORAGE_TYPE structure [VHD], VIRTUAL_STORAGE_TYPE_DEVICE_ISO, VIRTUAL_STORAGE_TYPE_DEVICE_UNKNOWN, VIRTUAL_STORAGE_TYPE_DEVICE_VHD, VIRTUAL_STORAGE_TYPE_DEVICE_VHDX, VIRTUAL_STORAGE_TYPE_VENDOR_MICROSOFT, VIRTUAL_STORAGE_TYPE_VENDOR_UNKNOWN, _VIRTUAL_STORAGE_TYPE, vdssys/PVIRTUAL_STORAGE_TYPE, vdssys/VIRTUAL_STORAGE_TYPE, vhd.virtual_storage_type, virtdisk/PVIRTUAL_STORAGE_TYPE, virtdisk/VIRTUAL_STORAGE_TYPE'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: VIRTUAL_STORAGE_TYPE, *PVIRTUAL_STORAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VIRTUAL_STORAGE_TYPE
 - virtdisk/_VIRTUAL_STORAGE_TYPE
 - PVIRTUAL_STORAGE_TYPE
 - virtdisk/PVIRTUAL_STORAGE_TYPE
 - VIRTUAL_STORAGE_TYPE
 - virtdisk/VIRTUAL_STORAGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - VIRTUAL_STORAGE_TYPE
---

# VIRTUAL_STORAGE_TYPE structure


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

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvdprovider-createvdisk">IVdsVdProvider::CreateVDisk</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_vdisk_properties">VDS_VDISK_PROPERTIES</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>