---
UID: NN:directml.IDMLDevice
title: IDMLDevice
description: Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects. (IDMLDevice)
helpviewer_keywords: ["IDMLDevice","IDMLDevice interface","IDMLDevice interface","described","direct3d12.idmldevice","directml/IDMLDevice"]
old-location: direct3d12\idmldevice.htm
tech.root: directml
ms.assetid: C6E13DEF-1FE1-416E-9917-ECE20FBCA401
ms.date: 11/04/2020
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
 - IDMLDevice
 - directml/IDMLDevice
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
 - IDMLDevice
---

## -description

Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects. The **IDMLDevice** interface inherits from [IDMLObject](/windows/win32/api/directml/nn-directml-idmlobject).

A DirectML device is always associated with exactly one underlying Direct3D 12 device. All objects created by the DirectML device maintain a strong reference to their parent device. Unlike the Direct3D 12 device, the DML device is not a singleton. Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device. However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.

This object is thread-safe.

## -see-also

[IDMLObject](/windows/win32/api/directml/nn-directml-idmlobject)
