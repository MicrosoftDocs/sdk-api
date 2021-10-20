---
UID: NN:mfidl.IMFCameraOcclusionStateMonitor
tech.root: mf
title: IMFCameraOcclusionStateMonitor
ms.date: 05/25/2021
targetos: Windows
description: Monitors the occlusion state of a camera device.
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
 - IMFCameraOcclusionStateMonitor
f1_keywords:
 - IMFCameraOcclusionStateMonitor
 - mfidl/IMFCameraOcclusionStateMonitor
dev_langs:
 - c++
---

## -description

Monitors the occlusion state of a camera device.

## -remarks

Many devices provide mechanisms, such as a mechanical shutter, that allow the user to occlude the camera device for privacy. Other devices may occlude the camera in certain postures. This interface allows applications to receive notifications when the occlusion state of the camera changes so they can disable or modify their camera capture behavior when the camera is occluded. Note that some devices may have a mechanical camera shutter without a mechanism for sensing or reporting the state of the shutter, and therefore the camera occlusion APIs are unable to provide occlusion information on these devices. Also, some devices may not have a dedicated camera shutter but will still update the occlusion status of the camera based on whether the device lid is open or closed.

Create an instance of this interface by calling [MFCreateCameraOcclusionStateMonitor](nf-mfidl-mfcreatecameraocclusionstatemonitor.md), passing in an implementation of [IMFCameraOcclusionStateReportCallback](nn-mfidl-imfcameraocclusionstatereportcallback.md). After the monitor is started, the [IMFCameraOcclusionStateReportCallback::OnOcclusionStateReport](nf-mfidl-imfcameraocclusionstatereportcallback-onocclusionstatereport.md) callback is passed an instance of [IMFCameraOcclusionStateReport](nn-mfidl-imfcameraocclusionstatereport.md) on which you can call [GetOcclusionState](nf-mfidl-imfcameraocclusionstatereport-getocclusionstate.md) to get the new camera occlusion state.

## -see-also

[MFCreateCameraOcclusionStateMonitor](nf-mfidl-mfcreatecameraocclusionstatemonitor.md)
[IMFCameraOcclusionStateReportCallback](nn-mfidl-imfcameraocclusionstatereportcallback.md)
[IMFCameraOcclusionStateReport](nn-mfidl-imfcameraocclusionstatereport.md)

