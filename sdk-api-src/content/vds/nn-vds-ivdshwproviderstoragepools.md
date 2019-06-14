---
UID: NN:vds.IVdsHwProviderStoragePools
title: IVdsHwProviderStoragePools (vds.h)
author: windows-sdk-content
description: Provides methods to create LUNs in a storage pool and enumerate the storage pools managed by a hardware provider.
old-location: base\ivdshwproviderstoragepools.htm
tech.root: VDS
ms.assetid: c9db0e33-8cb1-41ba-8716-a8d70990fa3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderStoragePools, IVdsHwProviderStoragePools interface, IVdsHwProviderStoragePools interface,described, base.ivdshwproviderstoragepools, vds/IVdsHwProviderStoragePools, vdshwprv/IVdsHwProviderStoragePools
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
ms.custom: 19H1
---

# IVdsHwProviderStoragePools interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to create LUNs in a <a href="https://docs.microsoft.com/windows/desktop/VDS/storage-pool-object">storage pool</a> and enumerate the storage pools managed by a hardware provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderStoragePools</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderStoragePools</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-createluninstoragepool">CreateLunInStoragePool</a>
</td>
<td align="left" width="63%">
Creates a LUN in a storage pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-querymaxluncreatesizeinstoragepool">QueryMaxLunCreateSizeInStoragePool</a>
</td>
<td align="left" width="63%">
Returns the maximum size of the LUN that can be created in the storage pool based on the specified LUN type and hints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-querystoragepools">QueryStoragePools</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> enumeration object containing a list of the storage pools managed by the hardware provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsstoragepool">IVdsStoragePool</a>
 

 

