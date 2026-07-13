---
UID: NF:vds.IVdsAdvancedDisk.DeleteDriveLetter
title: IVdsAdvancedDisk::DeleteDriveLetter (vds.h)
description: Deletes a drive letter assigned to an OEM, ESP, or unknown partition.
helpviewer_keywords: ["DeleteDriveLetter","DeleteDriveLetter method [VDS]","DeleteDriveLetter method [VDS]","IVdsAdvancedDisk interface","IVdsAdvancedDisk interface [VDS]","DeleteDriveLetter method","IVdsAdvancedDisk.DeleteDriveLetter","IVdsAdvancedDisk::DeleteDriveLetter","base.ivdsadvanceddisk_deletedriveletter","vds/IVdsAdvancedDisk::DeleteDriveLetter"]
old-location: base\ivdsadvanceddisk_deletedriveletter.htm
tech.root: base
ms.assetid: 1df6bf7e-0155-463c-85e2-c879557bc044
ms.date: 12/05/2018
ms.keywords: DeleteDriveLetter, DeleteDriveLetter method [VDS], DeleteDriveLetter method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],DeleteDriveLetter method, IVdsAdvancedDisk.DeleteDriveLetter, IVdsAdvancedDisk::DeleteDriveLetter, base.ivdsadvanceddisk_deletedriveletter, vds/IVdsAdvancedDisk::DeleteDriveLetter
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
 - IVdsAdvancedDisk::DeleteDriveLetter
 - vds/IVdsAdvancedDisk::DeleteDriveLetter
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
 - IVdsAdvancedDisk.DeleteDriveLetter
---

# IVdsAdvancedDisk::DeleteDriveLetter


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Deletes a drive letter assigned to an OEM, ESP, or unknown partition.

## -parameters

### -param ullOffset [in]

The partition offset.

### -param wcLetter [in]

The drive letter to delete.

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
The drive letter was deleted successfully.

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
The partition is on a removable media; otherwise the partition is not an OEM, ESP or unknown partition.

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

VDS implements this method.

## -see-also

<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>