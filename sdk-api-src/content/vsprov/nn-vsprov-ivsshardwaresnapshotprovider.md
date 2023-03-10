---
UID: NN:vsprov.IVssHardwareSnapshotProvider
title: IVssHardwareSnapshotProvider (vsprov.h)
description: Contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the shadow copy process, and transport LUNs on a SAN.
helpviewer_keywords: ["IVssHardwareSnapshotProvider","IVssHardwareSnapshotProvider interface [VSS]","IVssHardwareSnapshotProvider interface [VSS]","described","base.ivsshardwaresnapshotprovider","vsprov/IVssHardwareSnapshotProvider"]
old-location: base\ivsshardwaresnapshotprovider.htm
tech.root: base
ms.assetid: 97fbb6bf-110e-4393-bf25-1ec378b91bdc
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProvider, IVssHardwareSnapshotProvider interface [VSS], IVssHardwareSnapshotProvider interface [VSS],described, base.ivsshardwaresnapshotprovider, vsprov/IVssHardwareSnapshotProvider
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssHardwareSnapshotProvider
 - vsprov/IVssHardwareSnapshotProvider
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
 - IVssHardwareSnapshotProvider
---

# IVssHardwareSnapshotProvider interface


## -description

The <b>IVssHardwareSnapshotProvider</b> 
   interface contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the 
   shadow copy process, and transport LUNs on a SAN. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b>IVssHardwareSnapshotProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssHardwareSnapshotProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
