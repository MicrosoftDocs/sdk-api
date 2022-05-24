---
UID: NF:mfidl.IMFCameraControlDefaultsCollection.GetControl
tech.root: mf
title: IMFCameraControlDefaultsCollection::GetControl
ms.date: 05/06/2022
targetos: Windows
description: Gets the control from the collection using the specified zero-based index.
prerelease: false
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
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
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
 - IMFCameraControlDefaultsCollection::GetControl
f1_keywords:
 - IMFCameraControlDefaultsCollection::GetControl
 - mfidl/IMFCameraControlDefaultsCollection::GetControl
dev_langs:
 - c++
helpviewer_keywords:
 - GetControl
---

## -description

Gets the control from the collection using the specified zero-based index.

## -parameters

### -param index [in]

The index of the control to retrieve.

### -param configuration

Receives a pointer to a [IMFCameraControlDefaults](nn-mfidl-imfcameracontroldefaults.md) instance representing the retrieved control.

## -returns

A HRESULT value, including the following.

| Value | Description |
|-------|-------------|
| S_OK | Success. |
| MF_E_INVALIDINDEX | The index was out of the allowed range.

## -remarks

The specified index must be less than the value returned by [GetControlCount](nf-mfidl-imfcameracontroldefaultscollection-getcontrolcount.md).

## -see-also

