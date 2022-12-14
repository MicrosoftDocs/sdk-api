---
UID: NF:vds.IVdsAdvancedDisk.GetPartitionProperties
title: IVdsAdvancedDisk::GetPartitionProperties (vds.h)
description: Returns the properties of the partition identified by the partition offset.
helpviewer_keywords: ["GetPartitionProperties","GetPartitionProperties method [VDS]","GetPartitionProperties method [VDS]","IVdsAdvancedDisk interface","IVdsAdvancedDisk interface [VDS]","GetPartitionProperties method","IVdsAdvancedDisk.GetPartitionProperties","IVdsAdvancedDisk::GetPartitionProperties","base.ivdsadvanceddisk_getpartitionproperties","vds/IVdsAdvancedDisk::GetPartitionProperties"]
old-location: base\ivdsadvanceddisk_getpartitionproperties.htm
tech.root: base
ms.assetid: 6dc96e7b-34e5-4366-8804-d40f111d77c2
ms.date: 12/05/2018
ms.keywords: GetPartitionProperties, GetPartitionProperties method [VDS], GetPartitionProperties method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],GetPartitionProperties method, IVdsAdvancedDisk.GetPartitionProperties, IVdsAdvancedDisk::GetPartitionProperties, base.ivdsadvanceddisk_getpartitionproperties, vds/IVdsAdvancedDisk::GetPartitionProperties
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAdvancedDisk::GetPartitionProperties
 - vds/IVdsAdvancedDisk::GetPartitionProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsAdvancedDisk.GetPartitionProperties
---

# IVdsAdvancedDisk::GetPartitionProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of the partition identified by the partition offset.

## -parameters

### -param ullOffset [in]

The partition offset.

### -param pPartitionProp [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a> structure allocated and passed in by the caller.

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
The method completed successfully.

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
</table>

## -remarks

This method returns information for all partition types.

## -see-also

<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a>