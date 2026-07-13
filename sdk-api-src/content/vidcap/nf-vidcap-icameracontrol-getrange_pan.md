---
UID: NF:vidcap.ICameraControl.getRange_Pan
title: ICameraControl::getRange_Pan (vidcap.h)
description: The getRange_Pan method returns the range of panning angles supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Pan method","ICameraControl.getRange_Pan","ICameraControl::getRange_Pan","ICameraControlgetRange_Pan","dshow.icameracontrol_getrange_pan","getRange_Pan","getRange_Pan method [DirectShow]","getRange_Pan method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Pan"]
old-location: dshow\icameracontrol_getrange_pan.htm
tech.root: dshow
ms.assetid: 390c6330-1eb4-4149-aabc-296b585b577a
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_Pan method, ICameraControl.getRange_Pan, ICameraControl::getRange_Pan, ICameraControlgetRange_Pan, dshow.icameracontrol_getrange_pan, getRange_Pan, getRange_Pan method [DirectShow], getRange_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Pan
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
 - ICameraControl::getRange_Pan
 - vidcap/ICameraControl::getRange_Pan
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
 - ICameraControl.getRange_Pan
---

# ICameraControl::getRange_Pan


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_Pan</code> method returns the range of panning angles supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum panning angle, in units of 1 arc second.

### -param pMax [out]

Receives the maximum panning angle, in units of 1 arc second.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default panning angle.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>