---
UID: NN:directml.IDMLPageable
title: IDMLPageable
author: windows-sdk-content
description: Implemented by objects that can be evicted from GPU memory, and hence that can be supplied to IDMLDevice::Evict and IDMLDevice::MakeResident.
old-location: direct3d12\idmlpageable.htm
tech.root: direct3d12
ms.assetid: A22F6DF1-E8A6-4FA8-B60C-5C566F0ED5CD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLPageable, IDMLPageable interface, IDMLPageable interface,described, direct3d12.idmlpageable, directml/IDMLPageable
ms.topic: interface
f1_keywords: ["directml/IDMLPageable"]
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLPageable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLPageable interface

## -description

Implemented by objects that can be evicted from GPU memory, and hence that can be supplied to [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice::MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). The **IDMLOperator** interface inherits from [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild).

## -see-also
[IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild)
