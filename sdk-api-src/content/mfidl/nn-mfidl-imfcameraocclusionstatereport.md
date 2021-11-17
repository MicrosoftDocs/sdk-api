---
UID: NN:mfidl.IMFCameraOcclusionStateReport
tech.root: mf
title: IMFCameraOcclusionStateReport
ms.date: 05/25/2021
targetos: Windows
description: Provides the camera occlusion state associated with a state change detected by an IMFCameraOcclusionStateMonitor.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraOcclusionStateReport
f1_keywords:
 - IMFCameraOcclusionStateReport
 - mfidl/IMFCameraOcclusionStateReport
dev_langs:
 - c++
---

## -description

Provides the camera occlusion state associated with a state change detected by an [IMFCameraOcclusionStateMonitor](nn-mfidl-imfcameraocclusionstatemonitor.md).

## -remarks

An instance of this class is passed into [IMFCameraOcclusionStateReportCallback::OnOcclusionStateReport](nf-mfidl-imfcameraocclusionstatereportcallback-onocclusionstatereport.md) callback. Register the callback interface when you create the camera occlusion state monitor with a call to [MFCreateCameraOcclusionStateMonitor](nf-mfidl-mfcreatecameraocclusionstatemonitor.md).

## -see-also

[IMFCameraOcclusionStateMonitor](nn-mfidl-imfcameraocclusionstatemonitor.md)
[IMFCameraOcclusionStateReportCallback::OnOcclusionStateReport](nf-mfidl-imfcameraocclusionstatereportcallback-onocclusionstatereport.md)
[MFCreateCameraOcclusionStateMonitor](nf-mfidl-mfcreatecameraocclusionstatemonitor.md)

