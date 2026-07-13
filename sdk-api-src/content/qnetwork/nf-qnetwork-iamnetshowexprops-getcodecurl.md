---
UID: NF:qnetwork.IAMNetShowExProps.GetCodecURL
title: IAMNetShowExProps::GetCodecURL (qnetwork.h)
description: The GetCodecURL method retrieves the URL where the codec may be downloaded.
helpviewer_keywords: ["GetCodecURL","GetCodecURL method [DirectShow]","GetCodecURL method [DirectShow]","IAMNetShowExProps interface","IAMNetShowExProps interface [DirectShow]","GetCodecURL method","IAMNetShowExProps.GetCodecURL","IAMNetShowExProps::GetCodecURL","IAMNetShowExPropsGetCodecURL","dshow.iamnetshowexprops_getcodecurl","qnetwork/IAMNetShowExProps::GetCodecURL"]
old-location: dshow\iamnetshowexprops_getcodecurl.htm
tech.root: dshow
ms.assetid: ad5672a8-2af9-45ef-b510-3c2f8948f64b
ms.date: 4/26/2023
ms.keywords: GetCodecURL, GetCodecURL method [DirectShow], GetCodecURL method [DirectShow],IAMNetShowExProps interface, IAMNetShowExProps interface [DirectShow],GetCodecURL method, IAMNetShowExProps.GetCodecURL, IAMNetShowExProps::GetCodecURL, IAMNetShowExPropsGetCodecURL, dshow.iamnetshowexprops_getcodecurl, qnetwork/IAMNetShowExProps::GetCodecURL
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowExProps::GetCodecURL
 - qnetwork/IAMNetShowExProps::GetCodecURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.GetCodecURL
---

# IAMNetShowExProps::GetCodecURL


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCodecURL</code> method retrieves the URL where the codec may be downloaded.

## -parameters

### -param CodecNum

Specifies the codec to query, indexed from zero. Call <b>get_CodecCount</b> to obtain the number of codecs.

### -param pbstrCodecURL

Pointer that receives the URL.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamnetshowexprops-get_codeccount">IAMNetShowExProps::get_CodecCount</a>