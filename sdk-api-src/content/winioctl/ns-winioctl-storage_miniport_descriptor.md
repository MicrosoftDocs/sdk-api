---
UID: NS:winioctl._STORAGE_MINIPORT_DESCRIPTOR
title: STORAGE_MINIPORT_DESCRIPTOR
description: Reserved for system use. (STORAGE_MINIPORT_DESCRIPTOR)
helpviewer_keywords: ["*PSTORAGE_MINIPORT_DESCRIPTOR","PSTORAGE_MINIPORT_DESCRIPTOR","PSTORAGE_MINIPORT_DESCRIPTOR structure pointer [Files]","STORAGE_MINIPORT_DESCRIPTOR","STORAGE_MINIPORT_DESCRIPTOR structure [Files]","StoragePortCodeSetReserved","StoragePortCodeSetSCSIport","StoragePortCodeSetStorport","fs.storage_miniport_descriptor","winioctl/PSTORAGE_MINIPORT_DESCRIPTOR","winioctl/STORAGE_MINIPORT_DESCRIPTOR"]
old-location: fs\storage_miniport_descriptor.htm
tech.root: fs
ms.assetid: b962666d-60ae-4e0b-813e-7b22e1670644
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_MINIPORT_DESCRIPTOR, PSTORAGE_MINIPORT_DESCRIPTOR, PSTORAGE_MINIPORT_DESCRIPTOR structure pointer [Files], STORAGE_MINIPORT_DESCRIPTOR, STORAGE_MINIPORT_DESCRIPTOR structure [Files], StoragePortCodeSetReserved, StoragePortCodeSetSCSIport, StoragePortCodeSetStorport, fs.storage_miniport_descriptor, winioctl/PSTORAGE_MINIPORT_DESCRIPTOR, winioctl/STORAGE_MINIPORT_DESCRIPTOR'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: STORAGE_MINIPORT_DESCRIPTOR, *PSTORAGE_MINIPORT_DESCRIPTOR
req.redist: 
f1_keywords:
 - _STORAGE_MINIPORT_DESCRIPTOR
 - winioctl/_STORAGE_MINIPORT_DESCRIPTOR
 - PSTORAGE_MINIPORT_DESCRIPTOR
 - winioctl/PSTORAGE_MINIPORT_DESCRIPTOR
 - STORAGE_MINIPORT_DESCRIPTOR
 - winioctl/STORAGE_MINIPORT_DESCRIPTOR
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
 - STORAGE_MINIPORT_DESCRIPTOR
---

# STORAGE_MINIPORT_DESCRIPTOR structure


## -description

Reserved for system use.

## -struct-fields

### -field Version

Contains the size of this structure, in bytes. The value of this member will change as members are added to 
      the structure.

### -field Size

Specifies the total size of the data returned, in bytes. This may include data that follows this 
      structure.

### -field Portdriver

Type of port driver as enumerated by the 
     <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_port_code_set">STORAGE_PORT_CODE_SET</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="StoragePortCodeSetReserved"></a><a id="storageportcodesetreserved"></a><a id="STORAGEPORTCODESETRESERVED"></a><dl>
<dt><b>StoragePortCodeSetReserved</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Indicates an unknown storage adapter driver type.

</td>
</tr>
<tr>
<td width="40%"><a id="StoragePortCodeSetStorport"></a><a id="storageportcodesetstorport"></a><a id="STORAGEPORTCODESETSTORPORT"></a><dl>
<dt><b>StoragePortCodeSetStorport</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Storage adapter driver is a Storport-miniport driver.

</td>
</tr>
<tr>
<td width="40%"><a id="StoragePortCodeSetSCSIport"></a><a id="storageportcodesetscsiport"></a><a id="STORAGEPORTCODESETSCSIPORT"></a><dl>
<dt><b>StoragePortCodeSetSCSIport</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Storage adapter driver is a SCSI Port-miniport driver.

</td>
</tr>
</table>

### -field LUNResetSupported

Indicates whether a LUN reset is supported.

### -field TargetResetSupported

Indicates whether a target reset is supported.

### -field IoTimeoutValue

### -field ExtraIoInfoSupported

### -field Reserved0

### -field Reserved1

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_port_code_set">STORAGE_PORT_CODE_SET</a>
