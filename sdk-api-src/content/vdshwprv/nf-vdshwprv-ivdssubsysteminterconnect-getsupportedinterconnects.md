---
UID: NF:vdshwprv.IVdsSubSystemInterconnect.GetSupportedInterconnects
title: IVdsSubSystemInterconnect::GetSupportedInterconnects (vdshwprv.h)
description: Returns the interconnect types that the subsystem supports.
helpviewer_keywords: ["GetSupportedInterconnects","GetSupportedInterconnects method","GetSupportedInterconnects method","IVdsSubSystemInterconnect interface","IVdsSubSystemInterconnect interface","GetSupportedInterconnects method","IVdsSubSystemInterconnect.GetSupportedInterconnects","IVdsSubSystemInterconnect::GetSupportedInterconnects","base.ivdssubsysteminterconnect_getsupportedinterconnects","vds/IVdsSubSystemInterconnect::GetSupportedInterconnects","vdshwprv/IVdsSubSystemInterconnect::GetSupportedInterconnects"]
old-location: base\ivdssubsysteminterconnect_getsupportedinterconnects.htm
tech.root: base
ms.assetid: 5e8e69b4-023d-49f7-a363-bae1ae9536ac
ms.date: 12/05/2018
ms.keywords: GetSupportedInterconnects, GetSupportedInterconnects method, GetSupportedInterconnects method,IVdsSubSystemInterconnect interface, IVdsSubSystemInterconnect interface,GetSupportedInterconnects method, IVdsSubSystemInterconnect.GetSupportedInterconnects, IVdsSubSystemInterconnect::GetSupportedInterconnects, base.ivdssubsysteminterconnect_getsupportedinterconnects, vds/IVdsSubSystemInterconnect::GetSupportedInterconnects, vdshwprv/IVdsSubSystemInterconnect::GetSupportedInterconnects
f1_keywords:
- vdshwprv/IVdsSubSystemInterconnect.GetSupportedInterconnects
dev_langs:
- c++
req.header: vdshwprv.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsSubSystemInterconnect.GetSupportedInterconnects
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSubSystemInterconnect::GetSupportedInterconnects


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the interconnect types that the subsystem supports.


## -parameters




### -param pulSupportedInterconnectsFlag [out]

A pointer to a caller-allocated <b>ULONG</b> value that receives a bitmask of <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_interconnect_flag">VDS_INTERCONNECT_FLAG</a> flags, one for each interconnect type that the subsystem supports. This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsysteminterconnect">IVdsSubSystemInterconnect</a>
 

 

