---
UID: NF:vidcap.ICameraControl.getRange_Iris
title: ICameraControl::getRange_Iris (vidcap.h)
description: The getRange_Iris method returns the range of aperture settings supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Iris method","ICameraControl.getRange_Iris","ICameraControl::getRange_Iris","ICameraControlgetRange_Iris","dshow.icameracontrol_getrange_iris","getRange_Iris","getRange_Iris method [DirectShow]","getRange_Iris method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Iris"]
old-location: dshow\icameracontrol_getrange_iris.htm
tech.root: dshow
ms.assetid: 3f3bc5b0-18eb-470c-9922-1d401f43e269
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_Iris method, ICameraControl.getRange_Iris, ICameraControl::getRange_Iris, ICameraControlgetRange_Iris, dshow.icameracontrol_getrange_iris, getRange_Iris, getRange_Iris method [DirectShow], getRange_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Iris
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
 - ICameraControl::getRange_Iris
 - vidcap/ICameraControl::getRange_Iris
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
 - ICameraControl.getRange_Iris
---

# ICameraControl::getRange_Iris


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_Iris</code> method returns the range of aperture settings supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum aperture setting, in units of f-stop * 100.

### -param pMax [out]

Receives the maximum aperture setting, in units of f-stop * 100.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default aperture setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>