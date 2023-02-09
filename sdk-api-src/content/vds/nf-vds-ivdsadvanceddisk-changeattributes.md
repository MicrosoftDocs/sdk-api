---
UID: NF:vds.IVdsAdvancedDisk.ChangeAttributes
title: IVdsAdvancedDisk::ChangeAttributes (vds.h)
description: Modifies the attributes of the partition.
helpviewer_keywords: ["ChangeAttributes","ChangeAttributes method [VDS]","ChangeAttributes method [VDS]","IVdsAdvancedDisk interface","IVdsAdvancedDisk interface [VDS]","ChangeAttributes method","IVdsAdvancedDisk.ChangeAttributes","IVdsAdvancedDisk::ChangeAttributes","base.ivdsadvanceddisk_changeattributes","vds/IVdsAdvancedDisk::ChangeAttributes"]
old-location: base\ivdsadvanceddisk_changeattributes.htm
tech.root: base
ms.assetid: 0345a4b1-bbe1-4e59-9a04-bb40ff6db954
ms.date: 12/05/2018
ms.keywords: ChangeAttributes, ChangeAttributes method [VDS], ChangeAttributes method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],ChangeAttributes method, IVdsAdvancedDisk.ChangeAttributes, IVdsAdvancedDisk::ChangeAttributes, base.ivdsadvanceddisk_changeattributes, vds/IVdsAdvancedDisk::ChangeAttributes
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAdvancedDisk::ChangeAttributes
 - vds/IVdsAdvancedDisk::ChangeAttributes
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
 - IVdsAdvancedDisk.ChangeAttributes
---

# IVdsAdvancedDisk::ChangeAttributes


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Modifies the attributes of the partition.

## -parameters

### -param ullOffset [in]

The partition offset.

### -param para [in]

The attribute parameters defined by  the <a href="/windows/desktop/api/vds/ns-vds-change_attributes_parameters">CHANGE_ATTRIBUTES_PARAMETERS</a> structure.

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
The parameter was changed successfully.

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
The operation is not supported on dynamic disks, or the disk is  removable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The partition is an extended partition. Extended partitions have no attributes to change.

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

For GPT disks, this method changes the hidden, read only, and no drive letter  attributes. For MBR disks, the method controls whether the boot indicator bit is active.

## -see-also

<a href="/windows/desktop/api/vds/ns-vds-change_attributes_parameters">CHANGE_ATTRIBUTES_PARAMETERS</a>



<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>