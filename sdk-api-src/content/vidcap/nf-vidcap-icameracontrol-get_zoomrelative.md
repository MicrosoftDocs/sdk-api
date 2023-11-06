---
UID: NF:vidcap.ICameraControl.get_ZoomRelative
title: ICameraControl::get_ZoomRelative (vidcap.h)
description: The get_ZoomRelative method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_ZoomRelative method","ICameraControl.get_ZoomRelative","ICameraControl::get_ZoomRelative","ICameraControlget_ZoomRelative","dshow.icameracontrol_get_zoomrelative","get_ZoomRelative","get_ZoomRelative method [DirectShow]","get_ZoomRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_ZoomRelative"]
old-location: dshow\icameracontrol_get_zoomrelative.htm
tech.root: dshow
ms.assetid: c1926541-d7c7-4a16-bbe7-0d93dec89c67
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_ZoomRelative method, ICameraControl.get_ZoomRelative, ICameraControl::get_ZoomRelative, ICameraControlget_ZoomRelative, dshow.icameracontrol_get_zoomrelative, get_ZoomRelative, get_ZoomRelative method [DirectShow], get_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ZoomRelative
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
 - ICameraControl::get_ZoomRelative
 - vidcap/ICameraControl::get_ZoomRelative
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
 - ICameraControl.get_ZoomRelative
---

# ICameraControl::get_ZoomRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ZoomRelative</code> method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.

## -parameters

### -param pValue [out]

Receives the relative zoom. The size of the value represents the desired zoom speed; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_zoomrelative">ICameraControl::getRange_ZoomRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stopped.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Zoom lens moving in the telephoto direction.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Zoom lens moving in the wide angle direction.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>