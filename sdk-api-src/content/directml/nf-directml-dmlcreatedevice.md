---
UID: NF:directml.DMLCreateDevice
title: DMLCreateDevice function
description: Creates a DirectML device for a given Direct3D 12 device. (DMLCreateDevice)
helpviewer_keywords: ["DMLCreateDevice","DMLCreateDevice function","direct3d12.dmlcreatedevice","directml/DMLCreateDevice"]
old-location: direct3d12\dmlcreatedevice.htm
tech.root: directml
ms.assetid: B97EBDA2-83FE-4982-987E-E5C9E615065C
ms.date: 11/04/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMLCreateDevice
 - directml/DMLCreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DirectML.dll
api_name:
 - DMLCreateDevice
---

## -description

Creates a DirectML device for a given Direct3D 12 device.

## -parameters

### -param d3d12Device

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over. DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP. However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device. See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.

If the call to **DMLCreateDevice** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.

### -param flags

Type: <b>DML_CREATE_DEVICE_FLAGS</b>

A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>. This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

### -param ppv

Type: \_COM\_Outptr\_opt\_ <b>void**</b>

A pointer to a memory block that receives a pointer to the device. This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If the function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.

## -remarks

A newer version of this function, [DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1), was introduced in DirectML version 1.1.0. **DMLCreateDevice** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## -see-also

* [DMLCreateDevice1 function](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [DirectML version history](/windows/ai/directml/dml-version-history)
* [Using the DirectML debug layer](/windows/ai/directml/dml-debug-layer)
