---
UID: NF:vds.IVdsOpenVDisk.DetachAndDelete
title: IVdsOpenVDisk::DetachAndDelete (vds.h)
description: Detaches a virtual disk and deletes the backing files.
helpviewer_keywords: ["DetachAndDelete","DetachAndDelete method","DetachAndDelete method","IVdsOpenVDisk interface","IVdsOpenVDisk interface","DetachAndDelete method","IVdsOpenVDisk.DetachAndDelete","IVdsOpenVDisk::DetachAndDelete","base.ivdsopenvdisk_detachanddelete","vds/IVdsOpenVDisk::DetachAndDelete"]
old-location: base\ivdsopenvdisk_detachanddelete.htm
tech.root: base
ms.assetid: 79179da4-3c88-480b-bfb8-c4315fa56c4e
ms.date: 12/05/2018
ms.keywords: DetachAndDelete, DetachAndDelete method, DetachAndDelete method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,DetachAndDelete method, IVdsOpenVDisk.DetachAndDelete, IVdsOpenVDisk::DetachAndDelete, base.ivdsopenvdisk_detachanddelete, vds/IVdsOpenVDisk::DetachAndDelete
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsOpenVDisk::DetachAndDelete
 - vds/IVdsOpenVDisk::DetachAndDelete
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
 - IVdsOpenVDisk.DetachAndDelete
---

# IVdsOpenVDisk::DetachAndDelete


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Detaches a virtual disk and deletes the backing files.

## -parameters

### -param Flags [in]

An <b>DETACH_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be detached. Must be set to DETACH_VIRTUAL_DISK_FLAG_NONE.

### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being detached and deleted. For the Microsoft provider, this must be 0. This value must match the value that was specified for the <i>ProviderSpecificFlags</i> parameter of the <a href="/windows/desktop/api/vds/nf-vds-ivdsvdprovider-createvdisk">IVdsVdProvider::CreateVDisk</a> method when the virtual disk was created.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
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
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a>