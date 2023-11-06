---
UID: NF:vidcap.ICameraControl.getRange_ZoomRelative
title: ICameraControl::getRange_ZoomRelative (vidcap.h)
description: The getRange_ZoomRelative method returns the range of relative zoom levels supported by the camera. The relative zoom indicates the direction in which the lens is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_ZoomRelative method","ICameraControl.getRange_ZoomRelative","ICameraControl::getRange_ZoomRelative","ICameraControlgetRange_ZoomRelative","dshow.icameracontrol_getrange_zoomrelative","getRange_ZoomRelative","getRange_ZoomRelative method [DirectShow]","getRange_ZoomRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_ZoomRelative"]
old-location: dshow\icameracontrol_getrange_zoomrelative.htm
tech.root: dshow
ms.assetid: ea3460b8-b956-4dc9-bed7-f28714e1df11
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_ZoomRelative method, ICameraControl.getRange_ZoomRelative, ICameraControl::getRange_ZoomRelative, ICameraControlgetRange_ZoomRelative, dshow.icameracontrol_getrange_zoomrelative, getRange_ZoomRelative, getRange_ZoomRelative method [DirectShow], getRange_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_ZoomRelative
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
 - ICameraControl::getRange_ZoomRelative
 - vidcap/ICameraControl::getRange_ZoomRelative
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
 - ICameraControl.getRange_ZoomRelative
---

# ICameraControl::getRange_ZoomRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_ZoomRelative</code> method returns the range of relative zoom levels supported by the camera. The relative zoom indicates the direction in which the lens is moving.

## -parameters

### -param pMin [out]

Receives the minimum relative zoom.

### -param pMax [out]

Receives the maximum relative zoom.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default relative zoom.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>