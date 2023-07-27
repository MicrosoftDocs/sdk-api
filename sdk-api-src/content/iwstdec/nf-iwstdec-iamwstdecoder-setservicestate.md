---
UID: NF:iwstdec.IAMWstDecoder.SetServiceState
title: IAMWstDecoder::SetServiceState (iwstdec.h)
description: Applications use the SetServiceState method to assign the service state.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetServiceState method","IAMWstDecoder.SetServiceState","IAMWstDecoder::SetServiceState","IAMWstDecoderSetServiceState","SetServiceState","SetServiceState method [DirectShow]","SetServiceState method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setservicestate","iwstdec/IAMWstDecoder::SetServiceState"]
old-location: dshow\iamwstdecoder_setservicestate.htm
tech.root: dshow
ms.assetid: c65d056e-0f39-4372-9060-37859798cade
ms.date: 4/26/2023
ms.keywords: IAMWstDecoder interface [DirectShow],SetServiceState method, IAMWstDecoder.SetServiceState, IAMWstDecoder::SetServiceState, IAMWstDecoderSetServiceState, SetServiceState, SetServiceState method [DirectShow], SetServiceState method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setservicestate, iwstdec/IAMWstDecoder::SetServiceState
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IAMWstDecoder::SetServiceState
 - iwstdec/IAMWstDecoder::SetServiceState
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
 - IAMWstDecoder.SetServiceState
---

# IAMWstDecoder::SetServiceState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Applications use the <code>SetServiceState</code> method to assign the service state.

## -parameters

### -param State [in]

Specifies a member of an <a href="/previous-versions/windows/desktop/api/iwstdec/ne-iwstdec-am_wst_state">AM_WST_STATE</a> enumeration to assign the service state.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_WST_STATE_On</td>
<td>Closed captioning on.</td>
</tr>
<tr>
<td>AM_WST_STATE_Off</td>
<td>Closed captioning off.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <code>HRESULT</code> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>