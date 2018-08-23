---
UID: NF:vds.IVdsSwProvider.QueryPacks
title: IVdsSwProvider::QueryPacks
author: windows-sdk-content
description: Returns an enumeration object that contains all packs managed by the software provider.
old-location: base\ivdsswprovider_querypacks.htm
old-project: vds
ms.assetid: f30494d8-ae82-479d-a47a-7087129e7e6a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsSwProvider interface [VDS],QueryPacks method, IVdsSwProvider.QueryPacks, IVdsSwProvider::QueryPacks, QueryPacks, QueryPacks method [VDS], QueryPacks method [VDS],IVdsSwProvider interface, base.ivdsswprovider_querypacks, vds/IVdsSwProvider::QueryPacks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsSwProvider.QueryPacks
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSwProvider::QueryPacks


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an enumeration object that contains all packs managed by the software provider.


## -parameters




### -param ppEnum [out]

The address of the <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the packs  as <a href="https://msdn.microsoft.com/e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9">pack objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the   pack objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/0602d4d6-a31d-4425-ad21-a267c6e1dd7b">IVdsSwProvider</a>



<a href="https://msdn.microsoft.com/2d711ed8-9101-4e68-b085-b5df01515b5d">IVdsSwProvider::CreatePack</a>
 

 

