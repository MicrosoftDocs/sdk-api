---
UID: NF:vidcap.ICameraControl.get_IrisRelative
title: ICameraControl::get_IrisRelative (vidcap.h)
description: The get_IrisRelative method returns the camera's relative aperture setting. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_IrisRelative method","ICameraControl.get_IrisRelative","ICameraControl::get_IrisRelative","ICameraControlget_IrisRelative","dshow.icameracontrol_get_irisrelative","get_IrisRelative","get_IrisRelative method [DirectShow]","get_IrisRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_IrisRelative"]
old-location: dshow\icameracontrol_get_irisrelative.htm
tech.root: dshow
ms.assetid: 15f01c00-ff18-4d58-a03b-9293a8a6a68c
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_IrisRelative method, ICameraControl.get_IrisRelative, ICameraControl::get_IrisRelative, ICameraControlget_IrisRelative, dshow.icameracontrol_get_irisrelative, get_IrisRelative, get_IrisRelative method [DirectShow], get_IrisRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_IrisRelative
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
 - ICameraControl::get_IrisRelative
 - vidcap/ICameraControl::get_IrisRelative
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
 - ICameraControl.get_IrisRelative
---

# ICameraControl::get_IrisRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_IrisRelative</code> method returns the camera's relative aperture setting. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pValue [out]

Receives the relative aperture setting. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_irisrelative">ICameraControl::getRange_IrisRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Default aperture setting.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Open by one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Close by one step.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>