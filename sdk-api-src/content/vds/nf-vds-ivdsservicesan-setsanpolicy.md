---
UID: NF:vds.IVdsServiceSAN.SetSANPolicy
title: IVdsServiceSAN::SetSANPolicy (vds.h)
description: Sets the disk SAN policy for the operating system.helpviewer_keywords: ["IVdsServiceSAN interface","SetSANPolicy method","IVdsServiceSAN.SetSANPolicy","IVdsServiceSAN::SetSANPolicy","SetSANPolicy","SetSANPolicy method","SetSANPolicy method","IVdsServiceSAN interface","base.ivdsservicesan_setsanpolicy","vds/IVdsServiceSAN::SetSANPolicy"]
old-location: base\ivdsservicesan_setsanpolicy.htm
tech.root: VDS
ms.assetid: e5cb0b5e-d181-44a7-8416-e9f8fb575423
ms.date: 12/05/2018
ms.keywords: IVdsServiceSAN interface,SetSANPolicy method, IVdsServiceSAN.SetSANPolicy, IVdsServiceSAN::SetSANPolicy, SetSANPolicy, SetSANPolicy method, SetSANPolicy method,IVdsServiceSAN interface, base.ivdsservicesan_setsanpolicy, vds/IVdsServiceSAN::SetSANPolicy
f1_keywords:
- vds/IVdsServiceSAN.SetSANPolicy
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- IVdsServiceSAN.SetSANPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceSAN::SetSANPolicy


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the disk <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_san_policy">SAN policy</a> for the operating system.


## -parameters




### -param SanPolicy [in]

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_san_policy">VDS_SAN_POLICY</a> enumeration that specifies the SAN policy.


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
<dt><b>VDS_E_SET_SAN_POLICY</b></dt>
</dl>
</td>
<td width="60%">
A driver error was reported when setting the SAN policy.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsservicesan">IVdsServiceSAN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservicesan-getsanpolicy">IVdsServiceSAN::GetSANPolicy</a>
 

 

