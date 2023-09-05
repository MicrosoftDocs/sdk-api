---
UID: NF:qnetwork.IAMNetShowExProps.get_Bandwidth
title: IAMNetShowExProps::get_Bandwidth (qnetwork.h)
description: The get_Bandwidth method retrieves the bandwidth.
helpviewer_keywords: ["IAMNetShowExProps interface [DirectShow]","get_Bandwidth method","IAMNetShowExProps.get_Bandwidth","IAMNetShowExProps::get_Bandwidth","IAMNetShowExPropsget_Bandwidth","dshow.iamnetshowexprops_get_bandwidth","get_Bandwidth","get_Bandwidth method [DirectShow]","get_Bandwidth method [DirectShow]","IAMNetShowExProps interface","qnetwork/IAMNetShowExProps::get_Bandwidth"]
old-location: dshow\iamnetshowexprops_get_bandwidth.htm
tech.root: dshow
ms.assetid: 042ddea5-c17a-4cd6-a18d-9a3b65bf11b7
ms.date: 4/26/2023
ms.keywords: IAMNetShowExProps interface [DirectShow],get_Bandwidth method, IAMNetShowExProps.get_Bandwidth, IAMNetShowExProps::get_Bandwidth, IAMNetShowExPropsget_Bandwidth, dshow.iamnetshowexprops_get_bandwidth, get_Bandwidth, get_Bandwidth method [DirectShow], get_Bandwidth method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_Bandwidth
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
 - IAMNetShowExProps::get_Bandwidth
 - qnetwork/IAMNetShowExProps::get_Bandwidth
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
 - IAMNetShowExProps.get_Bandwidth
---

# IAMNetShowExProps::get_Bandwidth


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Bandwidth</code> method retrieves the bandwidth.

## -parameters

### -param pBandwidth

Pointer to a variable that receives the bandwidth.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>