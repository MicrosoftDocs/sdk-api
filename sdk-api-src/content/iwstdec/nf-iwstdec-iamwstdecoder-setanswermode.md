---
UID: NF:iwstdec.IAMWstDecoder.SetAnswerMode
title: IAMWstDecoder::SetAnswerMode (iwstdec.h)
description: Downstream filters use the SetAnswerMode method to assign the current answer mode.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetAnswerMode method","IAMWstDecoder.SetAnswerMode","IAMWstDecoder::SetAnswerMode","IAMWstDecoderSetAnswerMode","SetAnswerMode","SetAnswerMode method [DirectShow]","SetAnswerMode method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setanswermode","iwstdec/IAMWstDecoder::SetAnswerMode"]
old-location: dshow\iamwstdecoder_setanswermode.htm
tech.root: dshow
ms.assetid: d26b22d2-2c88-4347-80fb-aca8abae50ab
ms.date: 4/26/2023
ms.keywords: IAMWstDecoder interface [DirectShow],SetAnswerMode method, IAMWstDecoder.SetAnswerMode, IAMWstDecoder::SetAnswerMode, IAMWstDecoderSetAnswerMode, SetAnswerMode, SetAnswerMode method [DirectShow], SetAnswerMode method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setanswermode, iwstdec/IAMWstDecoder::SetAnswerMode
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
 - IAMWstDecoder::SetAnswerMode
 - iwstdec/IAMWstDecoder::SetAnswerMode
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
 - IAMWstDecoder.SetAnswerMode
---

# IAMWstDecoder::SetAnswerMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>SetAnswerMode</code> method to assign the current answer mode.

## -parameters

### -param bAnswer [in]

Specifies the current answer mode.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Hidden text exposed.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Hidden text not exposed.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>