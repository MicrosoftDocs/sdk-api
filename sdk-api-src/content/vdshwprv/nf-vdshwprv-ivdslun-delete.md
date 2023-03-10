---
UID: NF:vdshwprv.IVdsLun.Delete
title: IVdsLun::Delete (vdshwprv.h)
description: The IVdsLun::Delete (vdshwprv.h) method deletes the LUN and all of its plexes. Any data on the LUN is lost. VDS frees the extents allocated to the LUN.
helpviewer_keywords: ["Delete","Delete method [VDS]","Delete method [VDS]","IVdsLun interface","IVdsLun interface [VDS]","Delete method","IVdsLun.Delete","IVdsLun::Delete","base.ivdslun_delete","vds/IVdsLun::Delete","vdshwprv/IVdsLun::Delete"]
old-location: base\ivdslun_delete.htm
tech.root: base
ms.assetid: 21522c62-0b60-4c70-b2bd-7a33aa94d280
ms.date: 08/08/2022
ms.keywords: Delete, Delete method [VDS], Delete method [VDS],IVdsLun interface, IVdsLun interface [VDS],Delete method, IVdsLun.Delete, IVdsLun::Delete, base.ivdslun_delete, vds/IVdsLun::Delete, vdshwprv/IVdsLun::Delete
req.header: vdshwprv.h
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
 - IVdsLun::Delete
 - vdshwprv/IVdsLun::Delete
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
 - IVdsLun.Delete
---

# IVdsLun::Delete


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Deletes the LUN and all of its 
   plexes. Any data on the LUN is lost. VDS frees the extents allocated to the LUN.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information about 
        the array. Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> 
        method followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The LUN is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.
       

</td>
</tr>
</table>

## -remarks

If an application holds a reference to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a> interface 
    and calls <b>IVdsLun::Delete</b>, implementers should return 
    <b>VDS_E_OBJECT_DELETED</b> on subsequent calls to methods such as 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">GetProperties</a> on that interface. In this case, 
    the interface has an  outstanding reference and is valid, but the underlying object no longer exists.
   

If a LUN that is unmasked to a target machine is deleted, the LUN's visibility on that machine may not change until a bus rescan is performed. The VDS application on the target machine initiates the bus rescan by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-reenumerate">IVdsService::Reenumerate</a>. The initiating of the bus rescan is the responsibility of the VDS application, not the hardware provider.

If a method such as <b>IVdsLun::Delete</b> is called in one thread while <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-queryluns">IVdsSubSystem::QueryLuns</a> is called in another thread that is running simultaneously, the result could be a provider access violation. The hardware provider is responsible for serializing these methods as needed to minimize such synchronization issues.

The hardware provider is responsible for removing the LUN's partition information so that the LUN can be reused. If the LUN is an MBR disk, this is accomplished by writing zeros to the first and last 1 MB of the disk. For a GPT disk, zeros must be written to the first and last 16 KB of the disk.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>
