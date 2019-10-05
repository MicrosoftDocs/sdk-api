---
UID: NN:vds.IVdsStoragePool
title: IVdsStoragePool (vds.h)
author: windows-sdk-content
description: Provides methods to query information and enumerate related objects for a storage pool.
old-location: base\ivdsstoragepool.htm
tech.root: VDS
ms.assetid: 1518ab95-1f0a-4f28-b2ae-e75bb4d19790
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsStoragePool, IVdsStoragePool interface, IVdsStoragePool interface,described, base.ivdsstoragepool, vds/IVdsStoragePool, vdshwprv/IVdsStoragePool
ms.topic: interface
f1_keywords: 
 - "vds/IVdsStoragePool"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsStoragePool interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query information and enumerate related objects for a <a href="https://docs.microsoft.com/windows/desktop/VDS/storage-pool-object">storage pool</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsStoragePool</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsStoragePool</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Returns the attributes of a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getprovider">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the hardware provider that manages the storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-queryallocatedluns">QueryAllocatedLuns</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the allocated LUNs for a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-queryallocatedstoragepools">QueryAllocatedStoragePools</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the allocated storage pools that are managed by the provider.BD

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-querydriveextents">QueryDriveExtents</a>
</td>
<td align="left" width="63%">
Returns an array of the drive extents that are used by a storage pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderstoragepools">IVdsHwProviderStoragePools</a>
 

 

