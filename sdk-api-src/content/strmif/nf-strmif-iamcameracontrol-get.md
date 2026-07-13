---
UID: NF:strmif.IAMCameraControl.Get
title: IAMCameraControl::Get (strmif.h)
description: The Get method gets the current setting of a camera property.
helpviewer_keywords: ["Get","Get method [DirectShow]","Get method [DirectShow]","IAMCameraControl interface","IAMCameraControl interface [DirectShow]","Get method","IAMCameraControl.Get","IAMCameraControl::Get","IAMCameraControlGet","dshow.iamcameracontrol_get","strmif/IAMCameraControl::Get"]
old-location: dshow\iamcameracontrol_get.htm
tech.root: dshow
ms.assetid: 5a21f207-5fbb-44b2-82d2-89be29dbdf2c
ms.date: 4/26/2023
ms.keywords: Get, Get method [DirectShow], Get method [DirectShow],IAMCameraControl interface, IAMCameraControl interface [DirectShow],Get method, IAMCameraControl.Get, IAMCameraControl::Get, IAMCameraControlGet, dshow.iamcameracontrol_get, strmif/IAMCameraControl::Get
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMCameraControl::Get
 - strmif/IAMCameraControl::Get
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
 - IAMCameraControl.Get
---

# IAMCameraControl::Get


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Get</b> method gets the current setting of a camera property.

## -parameters

### -param Property [in]

Specifies the property to retrieve, as a value from the [CameraControlProperty](/windows/desktop/api/strmif/ne-strmif-cameracontrolproperty) enumeration.

### -param lValue [out]

Receives the value of the property.

### -param Flags [out]

Receives a member of the [CameraControlFlags](/windows/desktop/api/strmif/ne-strmif-cameracontrolflags) enumeration. The returned value indicates whether the setting is controlled manually or automatically.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamcameracontrol-set">IAMCameraControl::Set</a>