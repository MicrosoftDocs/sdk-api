---
UID: NN:vsprov.IVssHardwareSnapshotProviderEx
title: IVssHardwareSnapshotProviderEx (vsprov.h)
description: Provides an additional method used by VSS to notify hardware providers of LUN state changes.
helpviewer_keywords: ["IVssHardwareSnapshotProviderEx","IVssHardwareSnapshotProviderEx interface","IVssHardwareSnapshotProviderEx interface","described","base.ivsshardwaresnapshotproviderex","vsprov/IVssHardwareSnapshotProviderEx"]
old-location: base\ivsshardwaresnapshotproviderex.htm
tech.root: base
ms.assetid: aaf94823-845b-49cb-8599-962229fef4cb
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProviderEx, IVssHardwareSnapshotProviderEx interface, IVssHardwareSnapshotProviderEx interface,described, base.ivsshardwaresnapshotproviderex, vsprov/IVssHardwareSnapshotProviderEx
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssHardwareSnapshotProviderEx
 - vsprov/IVssHardwareSnapshotProviderEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssHardwareSnapshotProviderEx
---

# IVssHardwareSnapshotProviderEx interface


## -description

Provides an additional method used by VSS to notify hardware providers of LUN state changes. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b>IVssHardwareSnapshotProviderEx</b> interface inherits from <a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>. <b>IVssHardwareSnapshotProviderEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
