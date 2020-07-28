---
UID: NF:vds.IVdsSubSystemIscsi.QueryTargets
title: IVdsSubSystemIscsi::QueryTargets (vds.h)
description: Returns an object that enumerates the iSCSI targets of the subsystem.
helpviewer_keywords: ["IVdsSubSystemIscsi interface [VDS]","QueryTargets method","IVdsSubSystemIscsi.QueryTargets","IVdsSubSystemIscsi::QueryTargets","QueryTargets","QueryTargets method [VDS]","QueryTargets method [VDS]","IVdsSubSystemIscsi interface","base.ivdssubsystemiscsi_querytargets","vds/IVdsSubSystemIscsi::QueryTargets","vdshwprv/IVdsSubSystemIscsi::QueryTargets"]
old-location: base\ivdssubsystemiscsi_querytargets.htm
tech.root: base
ms.assetid: 86a89c23-beed-48d0-8d35-ed8dd39db3c6
ms.date: 12/05/2018
ms.keywords: IVdsSubSystemIscsi interface [VDS],QueryTargets method, IVdsSubSystemIscsi.QueryTargets, IVdsSubSystemIscsi::QueryTargets, QueryTargets, QueryTargets method [VDS], QueryTargets method [VDS],IVdsSubSystemIscsi interface, base.ivdssubsystemiscsi_querytargets, vds/IVdsSubSystemIscsi::QueryTargets, vdshwprv/IVdsSubSystemIscsi::QueryTargets
f1_keywords:
- vds/IVdsSubSystemIscsi.QueryTargets
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsSubSystemIscsi.QueryTargets
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsSubSystemIscsi::QueryTargets


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an object that enumerates the iSCSI targets of the subsystem.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the iSCSI targets  as <a href="https://docs.microsoft.com/windows/desktop/VDS/target-object">target objects</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the target objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
     


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The enumeration of targets was successfully returned. If the subsystem has no iSCSI targets, the enumeration 
        is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
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
<dt><b><b>VDS_E_OBJECT_STATUS_FAILED</b></b></dt>
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
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystemiscsi">IVdsSubSystemIscsi</a>
 

 

