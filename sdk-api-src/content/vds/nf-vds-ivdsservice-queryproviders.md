---
UID: NF:vds.IVdsService.QueryProviders
title: IVdsService::QueryProviders
author: windows-driver-content
description: Returns an enumeration object containing a list of the hardware and software providers known to VDS.
old-location: base\ivdsservice_queryproviders.htm
old-project: VDS
ms.assetid: 55171eb1-6fec-4651-914c-88d23e8d7849
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVdsService interface [VDS],QueryProviders method, IVdsService.QueryProviders, IVdsService::QueryProviders, QueryProviders, QueryProviders method [VDS], QueryProviders method [VDS],IVdsService interface, base.ivdsservice_queryproviders, vds/IVdsService::QueryProviders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsService.QueryProviders
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsService::QueryProviders


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an enumeration object containing a list of the hardware and software providers known to VDS.


## -parameters




### -param masks [in]

The provider mask enumerated by <a href="https://msdn.microsoft.com/849b3cbc-a1ed-438a-8fda-ada096fb8375">VDS_QUERY_PROVIDER_FLAG</a>. Callers can specify a software provider mask, a hardware provider mask, or both.


### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the providers  as <a href="https://msdn.microsoft.com/131e927d-d32a-44f6-8aae-28839cfa9e7d">provider objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the provider objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The enumeration is returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -remarks



To determine the provider type for hardware providers, call the <a href="https://msdn.microsoft.com/9a75e6af-fd3d-4770-bc6d-31ad4d995eee">IVdsHwProviderType2::GetProviderType2</a> method or the <a href="https://msdn.microsoft.com/e88fd2df-531d-46d8-a91b-9b9f8578e57b">IVdsHwProviderType::GetProviderType</a> method for each provider object.




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>



<a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a>



<a href="https://msdn.microsoft.com/849b3cbc-a1ed-438a-8fda-ada096fb8375">VDS_QUERY_PROVIDER_FLAG</a>
 

 

