---
UID: NN:vds.IVdsStoragePool
title: IVdsStoragePool (vds.h)
author: windows-sdk-content
description: Provides methods to query information and enumerate related objects for a storage pool.
old-location: base\ivdsstoragepool.htm
tech.root: VDS
ms.assetid: 1518ab95-1f0a-4f28-b2ae-e75bb4d19790
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsStoragePool, IVdsStoragePool interface, IVdsStoragePool interface,described, base.ivdsstoragepool, vds/IVdsStoragePool, vdshwprv/IVdsStoragePool
ms.topic: interface
req.header: vds.h
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
 - IVdsStoragePool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsStoragePool interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query information and enumerate related objects for a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsStoragePool</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsStoragePool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsStoragePool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44906c1f-ecb2-4701-9392-a9b5924e9d65">GetAttributes</a>
</td>
<td align="left" width="63%">
Returns the attributes of a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c37b5b1-4958-4b63-ba30-65b394dd05b7">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46265fca-eabd-4d42-b1fd-6a09c566cde9">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the hardware provider that manages the storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/348472ac-1b8b-4943-9b80-813616861e01">QueryAllocatedLuns</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the allocated LUNs for a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b6c447a-35e1-48ff-951c-b13ff5584c76">QueryAllocatedStoragePools</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the allocated storage pools that are managed by the provider.BD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91bae6e6-3718-4d82-ab8c-e489b9a105fe">QueryDriveExtents</a>
</td>
<td align="left" width="63%">
Returns an array of the drive extents that are used by a storage pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c9db0e33-8cb1-41ba-8716-a8d70990fa3e">IVdsHwProviderStoragePools</a>
 

 

