---
UID: NF:vds.IVdsService.QueryUnallocatedDisks
title: IVdsService::QueryUnallocatedDisks (vds.h)
description: Returns an enumeration object containing a list of the unallocated disks managed by VDS.
helpviewer_keywords: ["IVdsService interface [VDS]","QueryUnallocatedDisks method","IVdsService.QueryUnallocatedDisks","IVdsService::QueryUnallocatedDisks","QueryUnallocatedDisks","QueryUnallocatedDisks method [VDS]","QueryUnallocatedDisks method [VDS]","IVdsService interface","base.ivdsservice_queryunallocateddisks","vds/IVdsService::QueryUnallocatedDisks"]
old-location: base\ivdsservice_queryunallocateddisks.htm
tech.root: base
ms.assetid: d519c3d0-7c5a-4c0c-bad9-2429490f2212
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],QueryUnallocatedDisks method, IVdsService.QueryUnallocatedDisks, IVdsService::QueryUnallocatedDisks, QueryUnallocatedDisks, QueryUnallocatedDisks method [VDS], QueryUnallocatedDisks method [VDS],IVdsService interface, base.ivdsservice_queryunallocateddisks, vds/IVdsService::QueryUnallocatedDisks
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
 - IVdsService::QueryUnallocatedDisks
 - vds/IVdsService::QueryUnallocatedDisks
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
 - IVdsService.QueryUnallocatedDisks
---

# IVdsService::QueryUnallocatedDisks


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an enumeration object containing a list of the unallocated disks managed by VDS.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the disks  as <a href="/windows/desktop/VDS/disk-object">disk objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the disk objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The enumeration was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the 
        method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -remarks

An unallocated disk is not claimed by any 
    provider. It may or may not contain MBR or GPT partition format information. Often it is an uninitialized disk. If the disk status is <b>VDS_DS_ONLINE</b> or <b>VDS_DS_OFFLINE</b>, the disk is unallocated and uninitialized. If it is <b>VDS_DS_UNKNOWN</b>, <b>VDS_DS_NOT_READY</b>, <b>VDS_DS_FAILED</b>, or <b>VDS_DS_MISSING</b>, it is unallocated, but the VDS service cannot determine whether or not it is initialized, possibly because of problems with the disk.

To determine the disk status, see the <b>status</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> or <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structure for the disk.

If the disk status is <b>VDS_DS_ONLINE</b>, the disk can be added to a pack.

If the disk status is <b>VDS_DS_OFFLINE</b>, try to bring the disk online by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsdiskonline-online">IVdsDiskOnline::Online</a>. If the call to the <b>Online</b> method succeeds, the disk can be added to a pack. If the call to <b>Online</b> fails, the disk cannot be used.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>