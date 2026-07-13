---
UID: NF:strmif.IAMCameraControl.Set
title: IAMCameraControl::Set (strmif.h)
description: The Set method sets a specified property on the camera.
helpviewer_keywords: ["IAMCameraControl interface [DirectShow]","Set method","IAMCameraControl.Set","IAMCameraControl::Set","IAMCameraControlSet","Set","Set method [DirectShow]","Set method [DirectShow]","IAMCameraControl interface","dshow.iamcameracontrol_set","strmif/IAMCameraControl::Set"]
old-location: dshow\iamcameracontrol_set.htm
tech.root: dshow
ms.assetid: d896fb5e-a43b-4cb8-a5d1-4ce6e60831be
ms.date: 4/26/2023
ms.keywords: IAMCameraControl interface [DirectShow],Set method, IAMCameraControl.Set, IAMCameraControl::Set, IAMCameraControlSet, Set, Set method [DirectShow], Set method [DirectShow],IAMCameraControl interface, dshow.iamcameracontrol_set, strmif/IAMCameraControl::Set
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
 - IAMCameraControl::Set
 - strmif/IAMCameraControl::Set
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
 - IAMCameraControl.Set
---

# IAMCameraControl::Set


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Set</b> method sets a specified property on the camera.

## -parameters

### -param Property [in]

Specifies the property to set, as a value from the [CameraControlProperty](/windows/desktop/api/strmif/ne-strmif-cameracontrolproperty) enumeration.

### -param lValue [in]

Specifies the new value of the property.

### -param Flags [in]

Specifies the desired control setting, as a member of the [CameraControlFlags](/windows/desktop/api/strmif/ne-strmif-cameracontrolflags) enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>Flags</i> parameter is <b>CameraControl_Flags_Auto</b>, the method ignores the <i>lValue</i> parameter, as long as it's between the minimum and maximum values of the property.

## -see-also

<a href="/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamcameracontrol-get">IAMCameraControl::Get</a>
