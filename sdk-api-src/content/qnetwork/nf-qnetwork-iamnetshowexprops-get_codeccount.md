---
UID: NF:qnetwork.IAMNetShowExProps.get_CodecCount
title: IAMNetShowExProps::get_CodecCount (qnetwork.h)
description: The get_CodecCount method retrieves the number codecs needed to play the file.
helpviewer_keywords: ["IAMNetShowExProps interface [DirectShow]","get_CodecCount method","IAMNetShowExProps.get_CodecCount","IAMNetShowExProps::get_CodecCount","IAMNetShowExPropsget_CodecCount","dshow.iamnetshowexprops_get_codeccount","get_CodecCount","get_CodecCount method [DirectShow]","get_CodecCount method [DirectShow]","IAMNetShowExProps interface","qnetwork/IAMNetShowExProps::get_CodecCount"]
old-location: dshow\iamnetshowexprops_get_codeccount.htm
tech.root: dshow
ms.assetid: 7b16727d-565a-431e-8124-124d72816d65
ms.date: 4/26/2023
ms.keywords: IAMNetShowExProps interface [DirectShow],get_CodecCount method, IAMNetShowExProps.get_CodecCount, IAMNetShowExProps::get_CodecCount, IAMNetShowExPropsget_CodecCount, dshow.iamnetshowexprops_get_codeccount, get_CodecCount, get_CodecCount method [DirectShow], get_CodecCount method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_CodecCount
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
 - IAMNetShowExProps::get_CodecCount
 - qnetwork/IAMNetShowExProps::get_CodecCount
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
 - IAMNetShowExProps.get_CodecCount
---

# IAMNetShowExProps::get_CodecCount


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_CodecCount</code> method retrieves the number codecs needed to play the file.

## -parameters

### -param pCodecCount

Pointer to a variable that receives the number of codecs.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>