---
UID: NF:vds.IVdsHwProviderType.GetProviderType
title: IVdsHwProviderType::GetProviderType
author: windows-sdk-content
description: Retrieves the type of the hardware provider.
old-location: base\ivdshwprovidertype_getprovidertype.htm
tech.root: VDS
ms.assetid: e88fd2df-531d-46d8-a91b-9b9f8578e57b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetProviderType, GetProviderType method [VDS], GetProviderType method [VDS],IVdsHwProviderType interface, IVdsHwProviderType interface [VDS],GetProviderType method, IVdsHwProviderType.GetProviderType, IVdsHwProviderType::GetProviderType, base.ivdshwprovidertype_getprovidertype, vds/IVdsHwProviderType::GetProviderType, vdshwprv/IVdsHwProviderType::GetProviderType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVdsHwProviderType.GetProviderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsHwProviderType.GetProviderType
: 
---

# IVdsHwProviderType::GetProviderType


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the type of the hardware provider.


## -parameters




### -param pType [out]

A pointer to a caller-allocated variable that receives a <a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a> enumeration value that specifies the hardware provider type. This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://msdn.microsoft.com/24bd634e-96e1-4f2a-a70b-3aae734c75f9">IVdsHwProviderType</a>



<a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">IVdsService::QueryProviders</a>



<a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a>
 

 

