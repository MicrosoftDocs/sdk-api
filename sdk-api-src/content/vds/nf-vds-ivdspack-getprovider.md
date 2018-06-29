---
UID: NF:vds.IVdsPack.GetProvider
title: IVdsPack::GetProvider
author: windows-sdk-content
description: Returns the software provider associated with a pack.
old-location: base\ivdspack_getprovider.htm
old-project: VDS
ms.assetid: b6e7ca7c-b95f-457d-996b-b3c449b6ce6b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetProvider, GetProvider method [VDS], GetProvider method [VDS],IVdsPack interface, IVdsPack interface [VDS],GetProvider method, IVdsPack.GetProvider, IVdsPack::GetProvider, base.ivdspack_getprovider, vds/IVdsPack::GetProvider
ms.prod: windows
ms.technology: windows-sdk
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
 - IVdsPack.GetProvider
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsPack::GetProvider


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the software provider associated with a pack.


## -parameters




### -param ppProvider [out]

The address of an <a href="https://msdn.microsoft.com/c09aa32f-d859-44b1-8656-973ba1b6a167">IVdsProvider</a> interface pointer. Callers must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The provider object was returned successfully.

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




<a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a>



<a href="https://msdn.microsoft.com/c09aa32f-d859-44b1-8656-973ba1b6a167">IVdsProvider</a>
 

 

