---
UID: NF:vdshwprv.IVdsSubSystem.Reenumerate
title: IVdsSubSystem::Reenumerate (vdshwprv.h)
description: The IVdsSubSystem::Reenumerate (vdshwprv.h) method prompts the subsystem to scan its bus to discover newly-connected drives or newly-disconnected drives.
helpviewer_keywords: ["IVdsSubSystem interface [VDS]","Reenumerate method","IVdsSubSystem.Reenumerate","IVdsSubSystem::Reenumerate","Reenumerate","Reenumerate method [VDS]","Reenumerate method [VDS]","IVdsSubSystem interface","base.ivdssubsystem_reenumerate","vds/IVdsSubSystem::Reenumerate","vdshwprv/IVdsSubSystem::Reenumerate"]
old-location: base\ivdssubsystem_reenumerate.htm
tech.root: base
ms.assetid: 9d6118bb-7b13-4ae1-9faf-9c17ada20511
ms.date: 08/08/2022
ms.keywords: IVdsSubSystem interface [VDS],Reenumerate method, IVdsSubSystem.Reenumerate, IVdsSubSystem::Reenumerate, Reenumerate, Reenumerate method [VDS], Reenumerate method [VDS],IVdsSubSystem interface, base.ivdssubsystem_reenumerate, vds/IVdsSubSystem::Reenumerate, vdshwprv/IVdsSubSystem::Reenumerate
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
 - IVdsSubSystem::Reenumerate
 - vdshwprv/IVdsSubSystem::Reenumerate
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
 - IVdsSubSystem.Reenumerate
---

# IVdsSubSystem::Reenumerate


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Prompts the 
   subsystem to scan its bus to discover newly-connected drives or newly-disconnected drives.



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
       the array. Use the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
       followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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

Most subsystems detect new connections and disconnections automatically. However, for those that do not, this 
    method provides a means by which to initiate detection manually. This operation can take a long time to complete.

When this method detects a newly connected drive, the provider creates a new drive object for it. When the 
     method detects a newly disconnected drive, the provider preserves the old drive object until its last VDS 
     reference is removed, and then deletes the object.

Each object should have a unique and persistent identifier. An object ID must be a valid GUID. Implementers 
    should persist an object ID across each reenumeration by using this method for objects that exist both before and 
    after the reenumeration.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>
