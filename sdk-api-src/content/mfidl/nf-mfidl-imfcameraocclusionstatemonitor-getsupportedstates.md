---
UID: NF:mfidl.IMFCameraOcclusionStateMonitor.GetSupportedStates
tech.root: mf
title: IMFCameraOcclusionStateMonitor::GetSupportedStates
ms.date: 05/24/2021
targetos: Windows
description: Gets the occlusion states supported by the current device.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - IMFCameraOcclusionStateMonitor::GetSupportedStates
f1_keywords:
 - IMFCameraOcclusionStateMonitor::GetSupportedStates
 - mfidl/IMFCameraOcclusionStateMonitor::GetSupportedStates
dev_langs:
 - c++
---

## -description

Gets the occlusion states supported by the current device.

## -returns

A **DWORD** containing a bitwise OR combination of values from the [MFCameraOcclusionState](ne-mfidl-mfcameraocclusionstate.md) enumeration.

## -remarks

To get the current occlusion state, call the [IMFCameraOcclusionStateReport::GetOcclusionState](nf-mfidl-imfcameraocclusionstatereport-getocclusionstate.md) method on the [IMFCameraOcclusionStateReport](nn-mfidl-imfcameraocclusionstatereport.md) passed to the [IMFCameraOcclusionStateReportCallback::OnOcclusionStateReport](nf-mfidl-imfcameraocclusionstatereportcallback-onocclusionstatereport.md) callback.

## -see-also

[IMFCameraOcclusionStateReport](nn-mfidl-imfcameraocclusionstatereport.md)
[IMFCameraOcclusionStateReportCallback::OnOcclusionStateReport](nf-mfidl-imfcameraocclusionstatereportcallback-onocclusionstatereport.md)

