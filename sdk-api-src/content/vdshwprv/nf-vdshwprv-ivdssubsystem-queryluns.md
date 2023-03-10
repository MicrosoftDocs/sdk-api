---
UID: NF:vdshwprv.IVdsSubSystem.QueryLuns
title: IVdsSubSystem::QueryLuns (vdshwprv.h)
description: The IVdsSubSystem::QueryLuns (vdshwprv.h) method returns an enumeration of LUNs surfaced in the subsystem and applies to hardware provider objects only.
helpviewer_keywords: ["IVdsSubSystem interface [VDS]","QueryLuns method","IVdsSubSystem.QueryLuns","IVdsSubSystem::QueryLuns","QueryLuns","QueryLuns method [VDS]","QueryLuns method [VDS]","IVdsSubSystem interface","base.ivdssubsystem_queryluns","vds/IVdsSubSystem::QueryLuns","vdshwprv/IVdsSubSystem::QueryLuns"]
old-location: base\ivdssubsystem_queryluns.htm
tech.root: base
ms.assetid: b8e17085-03cd-40d1-accf-6ea5fa69de65
ms.date: 08/08/2022
ms.keywords: IVdsSubSystem interface [VDS],QueryLuns method, IVdsSubSystem.QueryLuns, IVdsSubSystem::QueryLuns, QueryLuns, QueryLuns method [VDS], QueryLuns method [VDS],IVdsSubSystem interface, base.ivdssubsystem_queryluns, vds/IVdsSubSystem::QueryLuns, vdshwprv/IVdsSubSystem::QueryLuns
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
 - IVdsSubSystem::QueryLuns
 - vdshwprv/IVdsSubSystem::QueryLuns
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
 - IVdsSubSystem.QueryLuns
---

# IVdsSubSystem::QueryLuns


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an 
   enumeration of LUNs surfaced in the subsystem. This method applies to hardware provider objects only.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the LUNs  as <a href="/windows/desktop/VDS/lun-object">LUN objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the LUN  objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
Returns the enumeration of LUNs in the subsystem. If the subsystem has no LUNs, the enumeration is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches 
        information about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method 
        to restore the cache.
       

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
The subsystem object is no longer present.

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
The subsystem is in a failed state and is unable to perform the requested operation.

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
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
    includes all LUNs in the subsystem, regardless of LUN masking.
   

Implementers must return an empty enumeration object for each subsystem with zero LUNs.

If this method is called in two separate threads that are running simultaneously, the results may be inconsistent. If it is called in one thread while a method such as <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-delete">IVdsLun::Delete</a> is called in another thread that is running simultaneously, the result could be a provider access violation. The hardware provider is responsible for serializing this query operation as needed to minimize such synchronization issues.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>
