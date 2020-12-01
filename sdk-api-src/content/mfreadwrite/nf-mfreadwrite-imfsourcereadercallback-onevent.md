---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnEvent
title: IMFSourceReaderCallback::OnEvent (mfreadwrite.h)
description: Called when the source reader receives certain events from the media source.
helpviewer_keywords: ["IMFSourceReaderCallback interface [Media Foundation]","OnEvent method","IMFSourceReaderCallback.OnEvent","IMFSourceReaderCallback::OnEvent","OnEvent","OnEvent method [Media Foundation]","OnEvent method [Media Foundation]","IMFSourceReaderCallback interface","mf.imfsourcereadercallback_onevent","mfreadwrite/IMFSourceReaderCallback::OnEvent"]
old-location: mf\imfsourcereadercallback_onevent.htm
tech.root: mf
ms.assetid: cbe85d0f-26a1-4526-bfe6-b6183812a271
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnEvent method, IMFSourceReaderCallback.OnEvent, IMFSourceReaderCallback::OnEvent, OnEvent, OnEvent method [Media Foundation], OnEvent method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onevent, mfreadwrite/IMFSourceReaderCallback::OnEvent
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFSourceReaderCallback::OnEvent
 - mfreadwrite/IMFSourceReaderCallback::OnEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback.OnEvent
---

# IMFSourceReaderCallback::OnEvent


## -description

Called when the source reader receives certain events from the media source.

## -parameters

### -param dwStreamIndex [in]

For stream events, the value is the zero-based index of the stream that sent the event. For source events, the value is <b>MF_SOURCE_READER_MEDIASOURCE</b>.

### -param pEvent [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of the event.

## -returns

Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.

## -remarks

In the current implementation,  the source reader uses this method to forward the following events to the application:

<ul>
<li>
<a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a>
</li>
<li>
<a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a>
</li>
<li>
<a href="/windows/desktop/medfound/meconnectend">MEConnectEnd</a>
</li>
<li>
<a href="/windows/desktop/medfound/meconnectstart">MEConnectStart</a>
</li>
<li>
<a href="/windows/desktop/medfound/meextendedtype">MEExtendedType</a>
</li>
<li>
<a href="/windows/desktop/medfound/mesourcecharacteristicschanged">MESourceCharacteristicsChanged</a>
</li>
<li>
<a href="/windows/desktop/medfound/mesourcemetadatachanged">MESourceMetadataChanged</a>
</li>
</ul>
This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback">IMFSourceReaderCallback</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>