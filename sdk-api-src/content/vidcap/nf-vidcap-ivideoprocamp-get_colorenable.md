---
UID: NF:vidcap.IVideoProcAmp.get_ColorEnable
title: IVideoProcAmp::get_ColorEnable (vidcap.h)
description: The get_ColorEnable method returns the camera's color-enable setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_ColorEnable method","IVideoProcAmp.get_ColorEnable","IVideoProcAmp::get_ColorEnable","IVideoProcAmpget_ColorEnable","dshow.ivideoprocamp_get_colorenable","get_ColorEnable","get_ColorEnable method [DirectShow]","get_ColorEnable method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_ColorEnable"]
old-location: dshow\ivideoprocamp_get_colorenable.htm
tech.root: dshow
ms.assetid: 6097b8cf-b46e-443d-8f32-46eb4a8f4de6
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],get_ColorEnable method, IVideoProcAmp.get_ColorEnable, IVideoProcAmp::get_ColorEnable, IVideoProcAmpget_ColorEnable, dshow.ivideoprocamp_get_colorenable, get_ColorEnable, get_ColorEnable method [DirectShow], get_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_ColorEnable
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoProcAmp::get_ColorEnable
 - vidcap/IVideoProcAmp::get_ColorEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.get_ColorEnable
---

# IVideoProcAmp::get_ColorEnable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ColorEnable</code> method returns the camera's color-enable setting.

## -parameters

### -param pValue [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Color disabled.</td>
</tr>
<tr>
<td>1</td>
<td>Color enabled.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>