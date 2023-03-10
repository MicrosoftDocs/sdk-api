---
UID: NE:mfidl.MFCameraOcclusionState
tech.root: mf
title: MFCameraOcclusionState
ms.date: 05/52/2021
targetos: Windows
description: Specifies the occlusion state of a camera.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCameraOcclusionState
f1_keywords:
 - MFCameraOcclusionState
 - mfidl/MFCameraOcclusionState
dev_langs:
 - c++
---

## -description

Specifies the occlusion state of a camera.

## -enum-fields

### -field MFCameraOcclusionState_Open

The camera is not occluded.

### -field MFCameraOcclusionState_OccludedByLid

The camera is occluded by the lid of the device.

### -field MFCameraOcclusionState_OccludedByCameraHardware

The camera is occluded by camera hardware.

## -remarks

A value from this enumeration is returned by [IMFCameraOcclusionStateReport::GetOcclusionState](nf-mfidl-imfcameraocclusionstatereport-getocclusionstate.md). To get the occlusion states that are supported on the current device, and therefore may be returned by **GetOcclusionState**, call [IMFCameraOcclusionStateMonitor::GetSupportedStates](nf-mfidl-imfcameraocclusionstatemonitor-getsupportedstates.md).

## -see-also

[IMFCameraOcclusionStateReport::GetOcclusionState](nf-mfidl-imfcameraocclusionstatereport-getocclusionstate.md)

[IMFCameraOcclusionStateMonitor::GetSupportedStates](nf-mfidl-imfcameraocclusionstatemonitor-getsupportedstates.md)

