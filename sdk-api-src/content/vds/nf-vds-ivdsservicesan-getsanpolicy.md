---
UID: NF:vds.IVdsServiceSAN.GetSANPolicy
title: IVdsServiceSAN::GetSANPolicy (vds.h)
description: Gets the disk SAN policy for the operating system.
helpviewer_keywords: ["GetSANPolicy","GetSANPolicy method","GetSANPolicy method","IVdsServiceSAN interface","IVdsServiceSAN interface","GetSANPolicy method","IVdsServiceSAN.GetSANPolicy","IVdsServiceSAN::GetSANPolicy","base.ivdsservicesan_getsanpolicy","vds/IVdsServiceSAN::GetSANPolicy"]
old-location: base\ivdsservicesan_getsanpolicy.htm
tech.root: base
ms.assetid: 59602d97-2fdf-4d1b-b158-e545619397e0
ms.date: 12/05/2018
ms.keywords: GetSANPolicy, GetSANPolicy method, GetSANPolicy method,IVdsServiceSAN interface, IVdsServiceSAN interface,GetSANPolicy method, IVdsServiceSAN.GetSANPolicy, IVdsServiceSAN::GetSANPolicy, base.ivdsservicesan_getsanpolicy, vds/IVdsServiceSAN::GetSANPolicy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsServiceSAN::GetSANPolicy
 - vds/IVdsServiceSAN::GetSANPolicy
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
 - IVdsServiceSAN.GetSANPolicy
---

# IVdsServiceSAN::GetSANPolicy


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Gets the disk <a href="/windows/desktop/api/vds/ne-vds-vds_san_policy">SAN policy</a> for the operating system.

## -parameters

### -param pSanPolicy [out]

A pointer to a variable that receives a value from the <a href="/windows/desktop/api/vds/ne-vds-vds_san_policy">VDS_SAN_POLICY</a> enumeration.

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
<dt><b>VDS_E_GET_SAN_POLICY</b></dt>
</dl>
</td>
<td width="60%">
A driver error was reported when getting the SAN policy.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservicesan">IVdsServiceSAN</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservicesan-setsanpolicy">IVdsServiceSAN::SetSANPolicy</a>