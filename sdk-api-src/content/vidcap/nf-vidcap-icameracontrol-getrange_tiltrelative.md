---
UID: NF:vidcap.ICameraControl.getRange_TiltRelative
title: ICameraControl::getRange_TiltRelative (vidcap.h)
description: The getRange_TiltRelative method returns the range of relative tilt angles supported by the camera. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_TiltRelative method","ICameraControl.getRange_TiltRelative","ICameraControl::getRange_TiltRelative","ICameraControlgetRange_TiltRelative","dshow.icameracontrol_getrange_tiltrelative","getRange_TiltRelative","getRange_TiltRelative method [DirectShow]","getRange_TiltRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_TiltRelative"]
old-location: dshow\icameracontrol_getrange_tiltrelative.htm
tech.root: dshow
ms.assetid: 8b78e961-8b05-4339-ad66-49f2d892d4dc
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_TiltRelative method, ICameraControl.getRange_TiltRelative, ICameraControl::getRange_TiltRelative, ICameraControlgetRange_TiltRelative, dshow.icameracontrol_getrange_tiltrelative, getRange_TiltRelative, getRange_TiltRelative method [DirectShow], getRange_TiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_TiltRelative
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICameraControl::getRange_TiltRelative
 - vidcap/ICameraControl::getRange_TiltRelative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.getRange_TiltRelative
---

# ICameraControl::getRange_TiltRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_TiltRelative</code> method returns the range of relative tilt angles supported by the camera. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pMin [out]

Receives the minimum relative tilt angle.

### -param pMax [out]

Receives the maximum relative title angle.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default relative tilt angle.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>