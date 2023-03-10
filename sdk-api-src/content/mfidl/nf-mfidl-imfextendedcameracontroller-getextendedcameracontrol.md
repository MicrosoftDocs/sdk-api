---
UID: NF:mfidl.IMFExtendedCameraController.GetExtendedCameraControl
title: IMFExtendedCameraController::GetExtendedCameraControl
ms.date: 11/4/2019
targetos: Windows
description: Gets an instance of IMFExtendedCameraControl, which allows an app to get the current capture device's extended property controls.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFExtendedCameraController::GetExtendedCameraControl
f1_keywords:
 - IMFExtendedCameraController::GetExtendedCameraControl
 - mfidl/IMFExtendedCameraController::GetExtendedCameraControl
dev_langs:
 - c++
---

## -description

Gets an instance of [IMFExtendedCameraControl](nn-mfidl-imfextendedcameracontrol.md), which allows an app to get the current capture device's extended property controls.

## -parameters

### -param dwStreamIndex

A **DWORD** indicating stream index to use for this property. Specify [MF_CAPTURE_ENGINE_MEDIASOURCE](/windows/win32/medfound/mf-capture-engine-mediasource-config) to indicate that the extended property is a filter-level property.

### -param ulPropertyId

The ID indicating the index for identifying the property within [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol
).

### -param ppControl

Receives a pointer to the **IMFExtendedCameraControl** instance that represents the requested control.

## -returns

Returns S_OK on success.

## -remarks

## -see-also

