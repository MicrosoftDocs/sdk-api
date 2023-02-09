---
UID: NF:vds.IVdsAdvancedDisk2.ChangePartitionType
title: IVdsAdvancedDisk2::ChangePartitionType (vds.h)
description: Changes the partition type on the disk at a specified byte offset.
helpviewer_keywords: ["ChangePartitionType","ChangePartitionType method","ChangePartitionType method","IVdsAdvancedDisk2 interface","IVdsAdvancedDisk2 interface","ChangePartitionType method","IVdsAdvancedDisk2.ChangePartitionType","IVdsAdvancedDisk2::ChangePartitionType","base.ivdsadvanceddisk2_changepartitiontype","vds/IVdsAdvancedDisk2::ChangePartitionType"]
old-location: base\ivdsadvanceddisk2_changepartitiontype.htm
tech.root: base
ms.assetid: 808a1e5a-d225-4b74-9764-3ad8cdc52ebe
ms.date: 12/05/2018
ms.keywords: ChangePartitionType, ChangePartitionType method, ChangePartitionType method,IVdsAdvancedDisk2 interface, IVdsAdvancedDisk2 interface,ChangePartitionType method, IVdsAdvancedDisk2.ChangePartitionType, IVdsAdvancedDisk2::ChangePartitionType, base.ivdsadvanceddisk2_changepartitiontype, vds/IVdsAdvancedDisk2::ChangePartitionType
req.header: vds.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAdvancedDisk2::ChangePartitionType
 - vds/IVdsAdvancedDisk2::ChangePartitionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAdvancedDisk2.ChangePartitionType
---

# IVdsAdvancedDisk2::ChangePartitionType


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Changes the partition type on the disk at a specified byte offset.

## -parameters

### -param ullOffset [in]

Byte offset of the partition from the beginning of the disk.  This offset must be the offset of the start of a partition.

### -param bForce [in]

Boolean value that indicates whether change will be forced.

### -param para [in]

Pointer to a <a href="/windows/desktop/api/vds/ns-vds-change_partition_type_parameters">CHANGE_PARTITION_TYPE_PARAMETERS</a> structure that contains the partition type that the partition at the location specified by the <i>ullOffset</i> parameter will be changed to.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The partition type was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The partition is in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INTERNAL_ERROR</b></dt>
<dt>0x80042448L</dt>
</dl>
</td>
<td width="60%">
An internal error occurred. Check the event log for more details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_PARTITION_TYPE</b></dt>
<dt>0x80042565L</dt>
</dl>
</td>
<td width="60%">
The specified partition type is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The changing of the partition type on dynamic disks is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The partition does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_LDM</b></dt>
<dt>0x8004258DL</dt>
</dl>
</td>
<td width="60%">
This operation is not supported on LDM partitions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_MSR</b></dt>
<dt>0x8004258CL</dt>
</dl>
</td>
<td width="60%">
This operation is not supported on MSR partitions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_STYLE_MISMATCH</b></dt>
<dt>0x80042571L</dt>
</dl>
</td>
<td width="60%">
The specified partition style does not match that of the disk.

</td>
</tr>
</table>

## -remarks

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk2">IVdsAdvancedDisk2</a>