---
UID: NF:vdshwprv.IVdsHwProviderType.GetProviderType
title: IVdsHwProviderType::GetProviderType (vdshwprv.h)
description: Retrieves the type of the hardware provider.helpviewer_keywords: ["GetProviderType","GetProviderType method [VDS]","GetProviderType method [VDS]","IVdsHwProviderType interface","IVdsHwProviderType interface [VDS]","GetProviderType method","IVdsHwProviderType.GetProviderType","IVdsHwProviderType::GetProviderType","base.ivdshwprovidertype_getprovidertype","vds/IVdsHwProviderType::GetProviderType","vdshwprv/IVdsHwProviderType::GetProviderType"]
old-location: base\ivdshwprovidertype_getprovidertype.htm
tech.root: VDS
ms.assetid: e88fd2df-531d-46d8-a91b-9b9f8578e57b
ms.date: 12/05/2018
ms.keywords: GetProviderType, GetProviderType method [VDS], GetProviderType method [VDS],IVdsHwProviderType interface, IVdsHwProviderType interface [VDS],GetProviderType method, IVdsHwProviderType.GetProviderType, IVdsHwProviderType::GetProviderType, base.ivdshwprovidertype_getprovidertype, vds/IVdsHwProviderType::GetProviderType, vdshwprv/IVdsHwProviderType::GetProviderType
f1_keywords:
- vdshwprv/IVdsHwProviderType.GetProviderType
dev_langs:
- c++
req.header: vdshwprv.h
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
- IVdsHwProviderType.GetProviderType
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsHwProviderType::GetProviderType


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the type of the hardware provider.


## -parameters




### -param pType [out]

A pointer to a caller-allocated variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a> enumeration value that specifies the hardware provider type. This parameter is required and cannot be <b>NULL</b>.


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
The hardware provider type was returned successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwprovidertype">IVdsHwProviderType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a>
 

 

