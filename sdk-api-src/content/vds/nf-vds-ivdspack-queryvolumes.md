---
UID: NF:vds.IVdsPack.QueryVolumes
title: IVdsPack::QueryVolumes (vds.h)
author: windows-sdk-content
description: Returns an object that enumerates the volumes in the pack.
old-location: base\ivdspack_queryvolumes.htm
tech.root: VDS
ms.assetid: 43f9972d-14a6-4674-bf90-741ad3a9eb0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsPack interface [VDS],QueryVolumes method, IVdsPack.QueryVolumes, IVdsPack::QueryVolumes, QueryVolumes, QueryVolumes method [VDS], QueryVolumes method [VDS],IVdsPack interface, base.ivdspack_queryvolumes, vds/IVdsPack::QueryVolumes
ms.topic: method
f1_keywords: 
 - "vds/IVdsPack.QueryVolumes"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsPack.QueryVolumes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsPack::QueryVolumes


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an object that enumerates the volumes in the pack.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the volumes  as <a href="https://docs.microsoft.com/windows/desktop/VDS/volume-object">volume objects</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the volume objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


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
The enumeration was returned successfully.

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
The dynamic provider cache is corrupt.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>
 

 

