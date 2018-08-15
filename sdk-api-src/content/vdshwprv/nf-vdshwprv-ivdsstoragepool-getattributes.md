---
UID: NF:vdshwprv.IVdsStoragePool.GetAttributes
title: IVdsStoragePool::GetAttributes
author: windows-sdk-content
description: Returns the attributes of a storage pool.
old-location: base\ivdsstoragepool_getattributes.htm
old-project: vds
ms.assetid: 44906c1f-ecb2-4701-9392-a9b5924e9d65
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetAttributes, GetAttributes method, GetAttributes method,IVdsStoragePool interface, IVdsStoragePool interface,GetAttributes method, IVdsStoragePool.GetAttributes, IVdsStoragePool::GetAttributes, base.ivdsstoragepool_getattributes, vds/IVdsStoragePool::GetAttributes, vdshwprv/IVdsStoragePool::GetAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.redist: 
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
 - IVdsStoragePool.GetAttributes
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsStoragePool::GetAttributes


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the attributes of a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.


## -parameters




### -param pStoragePoolAttributes [out]

The address of a caller-allocated <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a> structure that receives the storage pool attributes.


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
 

 

