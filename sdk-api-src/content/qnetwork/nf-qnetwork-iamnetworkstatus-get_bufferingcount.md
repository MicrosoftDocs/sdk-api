---
UID: NF:qnetwork.IAMNetworkStatus.get_BufferingCount
title: IAMNetworkStatus::get_BufferingCount (qnetwork.h)
description: The get_BufferingCount method retrieves the number of times the network source has buffered the data.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_BufferingCount method","IAMNetworkStatus.get_BufferingCount","IAMNetworkStatus::get_BufferingCount","IAMNetworkStatusget_BufferingCount","dshow.iamnetworkstatus_get_bufferingcount","get_BufferingCount","get_BufferingCount method [DirectShow]","get_BufferingCount method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_BufferingCount"]
old-location: dshow\iamnetworkstatus_get_bufferingcount.htm
tech.root: dshow
ms.assetid: 82c1994b-9326-48a7-8ff5-2b2df274b3e2
ms.date: 4/26/2023
ms.keywords: IAMNetworkStatus interface [DirectShow],get_BufferingCount method, IAMNetworkStatus.get_BufferingCount, IAMNetworkStatus::get_BufferingCount, IAMNetworkStatusget_BufferingCount, dshow.iamnetworkstatus_get_bufferingcount, get_BufferingCount, get_BufferingCount method [DirectShow], get_BufferingCount method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_BufferingCount
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
 - IAMNetworkStatus::get_BufferingCount
 - qnetwork/IAMNetworkStatus::get_BufferingCount
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
 - IAMNetworkStatus.get_BufferingCount
---

# IAMNetworkStatus::get_BufferingCount


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_BufferingCount</code> method retrieves the number of times the network source has buffered the data.

## -parameters

### -param pBufferingCount

Pointer to a variable that receives the buffering count.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>