---
UID: NF:vds.IVdsDisk.GetPack
title: IVdsDisk::GetPack (vds.h)
description: Returns the disk pack to which the current disk is a member.
helpviewer_keywords: ["GetPack","GetPack method [VDS]","GetPack method [VDS]","IVdsDisk interface","IVdsDisk interface [VDS]","GetPack method","IVdsDisk.GetPack","IVdsDisk::GetPack","base.ivdsdisk_getpack","vds/IVdsDisk::GetPack"]
old-location: base\ivdsdisk_getpack.htm
tech.root: base
ms.assetid: 52c7edb5-a92d-423d-8115-e8c3cccd95b5
ms.date: 12/05/2018
ms.keywords: GetPack, GetPack method [VDS], GetPack method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],GetPack method, IVdsDisk.GetPack, IVdsDisk::GetPack, base.ivdsdisk_getpack, vds/IVdsDisk::GetPack
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
 - IVdsDisk::GetPack
 - vds/IVdsDisk::GetPack
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
 - IVdsDisk.GetPack
---

# IVdsDisk::GetPack


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the disk pack to which the current disk is a member.

## -parameters

### -param ppPack [out]

The address of an <a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a> interface pointer, which VDS initializes on return. Callers must release the interface when the operation is complete.

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
The pointer to the disk pack address was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_NOT_INITIALIZED</b></dt>
<dt>0x80042417L</dt>
</dl>
</td>
<td width="60%">
The disk, unallocated and masked, is managed by VDS.

</td>
</tr>
</table>

## -remarks

A disk can be a member of only one disk pack.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>