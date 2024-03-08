---
UID: NF:strmif.IAMVfwCompressDialogs.SendDriverMessage
title: IAMVfwCompressDialogs::SendDriverMessage (strmif.h)
description: The SendDriverMessage method sends a driver-specific message. (IAMVfwCompressDialogs.SendDriverMessage)
helpviewer_keywords: ["IAMVfwCompressDialogs interface [DirectShow]","SendDriverMessage method","IAMVfwCompressDialogs.SendDriverMessage","IAMVfwCompressDialogs::SendDriverMessage","IAMVfwCompressDialogsSendDriverMessage","SendDriverMessage","SendDriverMessage method [DirectShow]","SendDriverMessage method [DirectShow]","IAMVfwCompressDialogs interface","dshow.iamvfwcompressdialogs_senddrivermessage","strmif/IAMVfwCompressDialogs::SendDriverMessage"]
old-location: dshow\iamvfwcompressdialogs_senddrivermessage.htm
tech.root: dshow
ms.assetid: b1558888-a8aa-416a-bb5b-a33a66dcb913
ms.date: 4/26/2023
ms.keywords: IAMVfwCompressDialogs interface [DirectShow],SendDriverMessage method, IAMVfwCompressDialogs.SendDriverMessage, IAMVfwCompressDialogs::SendDriverMessage, IAMVfwCompressDialogsSendDriverMessage, SendDriverMessage, SendDriverMessage method [DirectShow], SendDriverMessage method [DirectShow],IAMVfwCompressDialogs interface, dshow.iamvfwcompressdialogs_senddrivermessage, strmif/IAMVfwCompressDialogs::SendDriverMessage
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
 - IAMVfwCompressDialogs::SendDriverMessage
 - strmif/IAMVfwCompressDialogs::SendDriverMessage
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
 - IAMVfwCompressDialogs.SendDriverMessage
---

# IAMVfwCompressDialogs::SendDriverMessage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SendDriverMessage</code> method sends a driver-specific message.

## -parameters

### -param uMsg [in]

Message to send to the driver.

### -param dw1 [in]

Message data.

### -param dw2 [in]

Message data.

## -returns

Return value varies depending on the implementation within each driver.

## -remarks

You should never need to use this method. This method can send any private message to the video compressor (codec). Behavior might be undetermined in response to arbitrary messages; use this method at your own risk.

This method calls the Video for Windows video compression manager (VCM) <a href="/windows/desktop/api/vfw/nf-vfw-icsendmessage">ICSendMessage</a> function to send the message.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcompressdialogs">IAMVfwCompressDialogs Interface</a>
