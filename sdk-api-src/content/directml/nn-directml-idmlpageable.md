---
UID: NN:directml.IDMLPageable
title: IDMLPageable
description: Implemented by objects that can be evicted from GPU memory, and hence that can be supplied to IDMLDevice::Evict and IDMLDevice::MakeResident.
helpviewer_keywords: ["IDMLPageable","IDMLPageable interface","IDMLPageable interface","described","direct3d12.idmlpageable","directml/IDMLPageable"]
old-location: direct3d12\idmlpageable.htm
tech.root: directml
ms.assetid: A22F6DF1-E8A6-4FA8-B60C-5C566F0ED5CD
ms.date: 12/5/2018
ms.keywords: IDMLPageable, IDMLPageable interface, IDMLPageable interface,described, direct3d12.idmlpageable, directml/IDMLPageable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLPageable
 - directml/IDMLPageable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLPageable
---

## -description

Implemented by objects that can be evicted from GPU memory, and hence that can be supplied to [IDMLDevice::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident). The **IDMLOperator** interface inherits from [IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild).

## -see-also

[IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild)
