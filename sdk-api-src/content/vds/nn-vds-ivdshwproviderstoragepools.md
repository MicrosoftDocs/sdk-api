---
UID: NN:vds.IVdsHwProviderStoragePools
title: IVdsHwProviderStoragePools (vds.h)
description: The IVdsHwProviderStoragePools interface (vds.h) provides methods to create LUNs in a storage pool and enumerate storage pools managed by a hardware provider.
helpviewer_keywords: ["IVdsHwProviderStoragePools","IVdsHwProviderStoragePools interface","IVdsHwProviderStoragePools interface","described","base.ivdshwproviderstoragepools","vds/IVdsHwProviderStoragePools","vdshwprv/IVdsHwProviderStoragePools"]
old-location: base\ivdshwproviderstoragepools.htm
tech.root: base
ms.assetid: c9db0e33-8cb1-41ba-8716-a8d70990fa3e
ms.date: 08/08/2022
ms.keywords: IVdsHwProviderStoragePools, IVdsHwProviderStoragePools interface, IVdsHwProviderStoragePools interface,described, base.ivdshwproviderstoragepools, vds/IVdsHwProviderStoragePools, vdshwprv/IVdsHwProviderStoragePools
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsHwProviderStoragePools
 - vds/IVdsHwProviderStoragePools
dev_langs:
 - c++
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
---

# IVdsHwProviderStoragePools interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to create LUNs in a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a> and enumerate the storage pools managed by a hardware provider.

## -inheritance

The <b>IVdsHwProviderStoragePools</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderStoragePools</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsstoragepool">IVdsStoragePool</a>
