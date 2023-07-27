---
UID: NF:qnetwork.IAMChannelInfo.get_ChannelURL
title: IAMChannelInfo::get_ChannelURL (qnetwork.h)
description: The get_ChannelURL method retrieves the channel URL.
helpviewer_keywords: ["IAMChannelInfo interface [DirectShow]","get_ChannelURL method","IAMChannelInfo.get_ChannelURL","IAMChannelInfo::get_ChannelURL","IAMChannelInfoget_ChannelURL","dshow.iamchannelinfo_get_channelurl","get_ChannelURL","get_ChannelURL method [DirectShow]","get_ChannelURL method [DirectShow]","IAMChannelInfo interface","qnetwork/IAMChannelInfo::get_ChannelURL"]
old-location: dshow\iamchannelinfo_get_channelurl.htm
tech.root: dshow
ms.assetid: 27e1a315-db95-4f24-94b6-b10023e61e7a
ms.date: 4/26/2023
ms.keywords: IAMChannelInfo interface [DirectShow],get_ChannelURL method, IAMChannelInfo.get_ChannelURL, IAMChannelInfo::get_ChannelURL, IAMChannelInfoget_ChannelURL, dshow.iamchannelinfo_get_channelurl, get_ChannelURL, get_ChannelURL method [DirectShow], get_ChannelURL method [DirectShow],IAMChannelInfo interface, qnetwork/IAMChannelInfo::get_ChannelURL
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
 - IAMChannelInfo::get_ChannelURL
 - qnetwork/IAMChannelInfo::get_ChannelURL
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
 - IAMChannelInfo.get_ChannelURL
---

# IAMChannelInfo::get_ChannelURL


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ChannelURL</code> method retrieves the channel URL.

## -parameters

### -param pbstrChannelURL [out]

Pointer to a variable that receives the URL.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamchannelinfo">IAMChannelInfo Interface</a>