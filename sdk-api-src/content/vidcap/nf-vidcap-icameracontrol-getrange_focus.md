---
UID: NF:vidcap.ICameraControl.getRange_Focus
title: ICameraControl::getRange_Focus (vidcap.h)
description: The getRange_Focus method returns the range of focal distances supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Focus method","ICameraControl.getRange_Focus","ICameraControl::getRange_Focus","ICameraControlgetRange_Focus","dshow.icameracontrol_getrange_focus","getRange_Focus","getRange_Focus method [DirectShow]","getRange_Focus method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Focus"]
old-location: dshow\icameracontrol_getrange_focus.htm
tech.root: dshow
ms.assetid: f2da5473-82c3-4719-bba6-04a1793a98eb
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_Focus method, ICameraControl.getRange_Focus, ICameraControl::getRange_Focus, ICameraControlgetRange_Focus, dshow.icameracontrol_getrange_focus, getRange_Focus, getRange_Focus method [DirectShow], getRange_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Focus
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
 - ICameraControl::getRange_Focus
 - vidcap/ICameraControl::getRange_Focus
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
 - ICameraControl.getRange_Focus
---

# ICameraControl::getRange_Focus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_Focus</code> method returns the range of focal distances supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum focus distance, in millimeters.

### -param pMax [out]

Receives the maximum focus distance, in millimeters.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default focus distance.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>