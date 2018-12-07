---
UID: NN:vds.IVdsHwProviderStoragePools
title: IVdsHwProviderStoragePools
author: windows-sdk-content
description: Provides methods to create LUNs in a storage pool and enumerate the storage pools managed by a hardware provider.
old-location: base\ivdshwproviderstoragepools.htm
tech.root: vds
ms.assetid: c9db0e33-8cb1-41ba-8716-a8d70990fa3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsHwProviderStoragePools, IVdsHwProviderStoragePools interface, IVdsHwProviderStoragePools interface,described, base.ivdshwproviderstoragepools, vds/IVdsHwProviderStoragePools, vdshwprv/IVdsHwProviderStoragePools
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsHwProviderStoragePools
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsHwProviderStoragePools interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to create LUNs in a <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a> and enumerate the storage pools managed by a hardware provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderStoragePools</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsHwProviderStoragePools</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderStoragePools</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17377671-1a30-4aeb-bc89-3c1e3823d3fe">CreateLunInStoragePool</a>
</td>
<td align="left" width="63%">
Creates a LUN in a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37a802e2-4573-4f47-bf54-b2197034722d">QueryMaxLunCreateSizeInStoragePool</a>
</td>
<td align="left" width="63%">
Returns the maximum size of the LUN that can be created in the storage pool based on the specified LUN type and hints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/308c9821-927d-4b90-854d-b050f3730c22">QueryStoragePools</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> enumeration object containing a list of the storage pools managed by the hardware provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1518ab95-1f0a-4f28-b2ae-e75bb4d19790">IVdsStoragePool</a>
 

 

