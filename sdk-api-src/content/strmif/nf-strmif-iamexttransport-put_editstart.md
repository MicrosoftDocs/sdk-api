---
UID: NF:strmif.IAMExtTransport.put_EditStart
title: IAMExtTransport::put_EditStart (strmif.h)
description: The put_EditStart method activates the edit control on a capable transport.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_EditStart method","IAMExtTransport.put_EditStart","IAMExtTransport::put_EditStart","IAMExtTransportput_EditStart","dshow.iamexttransport_put_editstart","put_EditStart","put_EditStart method [DirectShow]","put_EditStart method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_EditStart"]
old-location: dshow\iamexttransport_put_editstart.htm
tech.root: dshow
ms.assetid: 1fd9c788-2ccb-47e5-bed8-fece9cfdf2a6
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],put_EditStart method, IAMExtTransport.put_EditStart, IAMExtTransport::put_EditStart, IAMExtTransportput_EditStart, dshow.iamexttransport_put_editstart, put_EditStart, put_EditStart method [DirectShow], put_EditStart method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_EditStart
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
 - IAMExtTransport::put_EditStart
 - strmif/IAMExtTransport::put_EditStart
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
 - IAMExtTransport.put_EditStart
---

# IAMExtTransport::put_EditStart


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_EditStart</code> method activates the edit control on a capable transport.



This method is not implemented.

## -parameters

### -param Value [in]

Specifies whether to active the edit control.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Activates the edit control.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Deactivates the edit control.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Use this method to manually enable edit control. Edit control is defined as the precise enabling of individual, or a set of, record tracks on a VCR; for example, a video-only insert edit, where only the video record head is enabled and a new video signal is recorded—the audio signal is left as is. Use this method to control "on the fly" editing on machines that have this feature.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_editstart">IAMExtTransport::get_EditStart</a>