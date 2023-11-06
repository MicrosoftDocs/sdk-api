---
UID: NF:vidcap.ICameraControl.put_ZoomRelative
title: ICameraControl::put_ZoomRelative (vidcap.h)
description: The put_ZoomRelative method sets the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_ZoomRelative method","ICameraControl.put_ZoomRelative","ICameraControl::put_ZoomRelative","ICameraControlput_ZoomRelative","dshow.icameracontrol_put_zoomrelative","put_ZoomRelative","put_ZoomRelative method [DirectShow]","put_ZoomRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_ZoomRelative"]
old-location: dshow\icameracontrol_put_zoomrelative.htm
tech.root: dshow
ms.assetid: 815f92c3-bfab-47d5-86dd-f9b2321d20eb
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_ZoomRelative method, ICameraControl.put_ZoomRelative, ICameraControl::put_ZoomRelative, ICameraControlput_ZoomRelative, dshow.icameracontrol_put_zoomrelative, put_ZoomRelative, put_ZoomRelative method [DirectShow], put_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_ZoomRelative
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
 - ICameraControl::put_ZoomRelative
 - vidcap/ICameraControl::put_ZoomRelative
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
 - ICameraControl.put_ZoomRelative
---

# ICameraControl::put_ZoomRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_ZoomRelative</code> method sets the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.

## -parameters

### -param Value [in]

Specifies the relative zoom. The size of the value represents the desired zoom speed; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_zoomrelative">ICameraControl::getRange_ZoomRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stop zoom lens motion.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start moving the zoom lens in the telephoto direction (initiate zoom-in).</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start moving the zoom lens in the wide angle direction (initiate zoom-out).</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>