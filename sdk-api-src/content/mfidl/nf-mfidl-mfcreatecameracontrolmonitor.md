---
UID: NF:mfidl.MFCreateCameraControlMonitor
tech.root: mf
title: MFCreateCameraControlMonitor
ms.date: 05/03/2022
targetos: Windows
description: Creates an instance of IMFCameraControlMonitor.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - MFCreateCameraControlMonitor
f1_keywords:
 - MFCreateCameraControlMonitor
 - mfidl/MFCreateCameraControlMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - MFCreateCameraControlMonitor
---

## -description

Creates an instance of [IMFCameraControlMonitor](nn-mfidl-imfcameracontrolmonitor.md)

## -parameters

### -param symbolicLink [in]

String symbolic link name of the video capture device that is active.

### -param callback [in]

Pointer to an object that implements the [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md) callback interface.

### -param ppCameraControlMonitor [out]

Receives a pointer to the created **IMFCameraControlMonitor** object.

## -returns

An HRESULT including the following:

| Value | Description | 
|-------|-------------|
| S_OK  | Success.  |
| E_INVALIDARG | The symbolic link specified in *symbolicLink* doesn't match a known camera device. |

## -remarks

The symbolic link can be obtained from an   [MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK](/windows/win32/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link) attribute returned by [MFEnumDeviceSources](nf-mfidl-mfenumdevicesources.md) or obtained by accessing the [DeviceInformation.Id](/uwp/api/windows.devices.enumeration.deviceinformation.id) property obtained through the [Windows.Devices.Enumeration](/uwp/api/windows.devices.enumeration) APIs.  

## -see-also

