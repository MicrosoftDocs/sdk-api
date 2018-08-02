---
UID: NF:vdshwprv.IVdsStoragePool.QueryAllocatedStoragePools
title: IVdsStoragePool::QueryAllocatedStoragePools
author: windows-sdk-content
description: Returns an object that enumerates the allocated storage pools that are managed by the provider.
old-location: base\ivdsstoragepool_queryallocatedstoragepools.htm
old-project: VDS
ms.assetid: 7b6c447a-35e1-48ff-951c-b13ff5584c76
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsStoragePool interface,QueryAllocatedStoragePools method, IVdsStoragePool.QueryAllocatedStoragePools, IVdsStoragePool::QueryAllocatedStoragePools, QueryAllocatedStoragePools, QueryAllocatedStoragePools method, QueryAllocatedStoragePools method,IVdsStoragePool interface, base.ivdsstoragepool_queryallocatedstoragepools, vds/IVdsStoragePool::QueryAllocatedStoragePools, vdshwprv/IVdsStoragePool::QueryAllocatedStoragePools
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsStoragePool.QueryAllocatedStoragePools
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsStoragePool::QueryAllocatedStoragePools


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an object that enumerates the allocated <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pools</a> that are managed by the provider.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the allocated storage pools. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the storage pool  objects when they are no longer needed by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.
     


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
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1518ab95-1f0a-4f28-b2ae-e75bb4d19790">IVdsStoragePool</a>
 

 

