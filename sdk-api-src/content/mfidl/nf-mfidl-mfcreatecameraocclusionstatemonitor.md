---
UID: NF:mfidl.MFCreateCameraOcclusionStateMonitor
tech.root: mf
title: MFCreateCameraOcclusionStateMonitor
ms.date: 05/25/2021
targetos: Windows
description: Creates a new instance of IMFCameraOcclusionStateMonitor which allows an application to receive notifications when the camera occlusion state changes.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - MFCreateCameraOcclusionStateMonitor
f1_keywords:
 - MFCreateCameraOcclusionStateMonitor
 - mfidl/MFCreateCameraOcclusionStateMonitor
dev_langs:
 - c++
---

## -description

Creates a new instance of [IMFCameraOcclusionStateMonitor](nn-mfidl-imfcameraocclusionstatemonitor.md) which allows an application to receive notifications when the camera occlusion state changes.

## -parameters

### -param symbolicLink

The symbolic link name of the video device for which occlusion state will be monitored. This value is enumerated through the standard Windows enumeration APIs such as [MFEnumDeviceSources](../mfidl/nf-mfidl-mfenumdevicesources.md) and [DeviceInformation](/uwp/api/Windows.Devices.Enumeration.DeviceInformation)

### -param callback

The [IMFCameraOcclusionStateReportCallback](nn-mfidl-imfcameraocclusionstatereportcallback.md) implemented by the client to receive camera occlusion state change notifications.

### -param occlusionStateMonitor

An output parameter that receives the [IMFCameraOcclusionStateMonitor](nf-mfidl-mfcreatecameraocclusionstatemonitor.md).

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG    | One or more parameters is nullptr |

## -remarks

## -see-also

