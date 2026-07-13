---
UID: NF:vidcap.ICameraControl.put_FocusRelative
title: ICameraControl::put_FocusRelative (vidcap.h)
description: The put_FocusRelative method sets the relative focus. The relative focus indicates the direction in which the lens group is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_FocusRelative method","ICameraControl.put_FocusRelative","ICameraControl::put_FocusRelative","ICameraControlput_FocusRelative","dshow.icameracontrol_put_focusrelative","put_FocusRelative","put_FocusRelative method [DirectShow]","put_FocusRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_FocusRelative"]
old-location: dshow\icameracontrol_put_focusrelative.htm
tech.root: dshow
ms.assetid: d40edc5d-8fa2-4e3a-8aab-c51da0ac8036
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_FocusRelative method, ICameraControl.put_FocusRelative, ICameraControl::put_FocusRelative, ICameraControlput_FocusRelative, dshow.icameracontrol_put_focusrelative, put_FocusRelative, put_FocusRelative method [DirectShow], put_FocusRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_FocusRelative
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
 - ICameraControl::put_FocusRelative
 - vidcap/ICameraControl::put_FocusRelative
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
 - ICameraControl.put_FocusRelative
---

# ICameraControl::put_FocusRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_FocusRelative</code> method sets the relative focus. The relative focus indicates the direction in which the lens group is moving.

## -parameters

### -param Value [in]

Specifies the relative focus. The size of the value represents the speed at which the focal point changes; a higher value represents a higher speed. To get the possible range of values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_focusrelative">ICameraControl::getRange_FocusRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stop focus motion.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start moving the focus closer to the object.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start moving the focus farther away from the object.</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>