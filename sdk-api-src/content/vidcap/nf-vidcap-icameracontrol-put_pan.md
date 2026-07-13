---
UID: NF:vidcap.ICameraControl.put_Pan
title: ICameraControl::put_Pan (vidcap.h)
description: The put_Pan method sets the camera's panning angle.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Pan method","ICameraControl.put_Pan","ICameraControl::put_Pan","ICameraControlput_Pan","dshow.icameracontrol_put_pan","put_Pan","put_Pan method [DirectShow]","put_Pan method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Pan"]
old-location: dshow\icameracontrol_put_pan.htm
tech.root: dshow
ms.assetid: 71dc3fe3-089c-46e8-a63b-7a638068d069
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_Pan method, ICameraControl.put_Pan, ICameraControl::put_Pan, ICameraControlput_Pan, dshow.icameracontrol_put_pan, put_Pan, put_Pan method [DirectShow], put_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Pan
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
 - ICameraControl::put_Pan
 - vidcap/ICameraControl::put_Pan
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
 - ICameraControl.put_Pan
---

# ICameraControl::put_Pan


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Pan</code> method sets the camera's panning angle.

## -parameters

### -param Value [in]

Specifies the panning angle, in degrees. Positive values are clockwise when viewing the camera from above, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_pan">ICameraControl::getRange_Pan</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>