---
UID: NN:directml.IDMLDebugDevice
title: IDMLDebugDevice
description: Controls the DirectML debug layers.
helpviewer_keywords: ["IDMLDebugDevice","IDMLDebugDevice interface","IDMLDebugDevice interface","described","direct3d12.idmldebugdevice","directml/IDMLDebugDevice"]
old-location: direct3d12\idmldebugdevice.htm
tech.root: directml
ms.assetid: 6602B70E-19EA-4C3D-B01C-16EC4830AB7F
ms.date: 12/5/2018
ms.keywords: IDMLDebugDevice, IDMLDebugDevice interface, IDMLDebugDevice interface,described, direct3d12.idmldebugdevice, directml/IDMLDebugDevice
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
 - IDMLDebugDevice
 - directml/IDMLDebugDevice
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
 - IDMLDebugDevice
---

## -description

Controls the DirectML debug layers. The <b>IDMLDebugDevice</b> interface inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.

This interface may be retrieved from the [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) via QueryInterface. This interface is available only if the DirectML device was created with the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag. DirectML sends messages to the <a href="/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a> associated with the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> passed in at [DMLCreateDevice](/windows/win32/api/directml/nf-directml-dmlcreatedevice); the Direct3D 12 info queue can be retrieved via QueryInterface on the <b>ID3D12Device</b>

This object is thread-safe.
