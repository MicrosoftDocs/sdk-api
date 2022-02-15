---
UID: NN:mfidl.IMFByteStreamBuffering
title: IMFByteStreamBuffering (mfidl.h)
description: Controls how a byte stream buffers data from a network.
helpviewer_keywords: ["IMFByteStreamBuffering","IMFByteStreamBuffering interface [Media Foundation]","IMFByteStreamBuffering interface [Media Foundation]","described","bbf9cdb1-5ec7-498a-aa59-85c24779547e","mf.imfbytestreambuffering","mfidl/IMFByteStreamBuffering"]
old-location: mf\imfbytestreambuffering.htm
tech.root: mf
ms.assetid: bbf9cdb1-5ec7-498a-aa59-85c24779547e
ms.date: 12/05/2018
ms.keywords: IMFByteStreamBuffering, IMFByteStreamBuffering interface [Media Foundation], IMFByteStreamBuffering interface [Media Foundation],described, bbf9cdb1-5ec7-498a-aa59-85c24779547e, mf.imfbytestreambuffering, mfidl/IMFByteStreamBuffering
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamBuffering
 - mfidl/IMFByteStreamBuffering
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamBuffering
---

# IMFByteStreamBuffering interface


## -description

Controls how a byte stream buffers data from a network.
        

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.

## -inheritance

The <b>IMFByteStreamBuffering</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamBuffering</b> also has these types of members:

## -remarks

If a byte stream implements this interface, a media source can use it to control how the byte stream buffers data. This interface is designed for byte streams that read data from a network.
      

A byte stream that implements this interface should also implement the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface. When the byte stream starts buffering, it sends an <a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event. When it stops buffering, it sends an <a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> event.
      

The byte stream must send a matching <a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> event for every <a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event. The byte stream must not send MEBufferingStarted events unless the media source has enabled buffering by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>TRUE</b>.
      

After the byte stream sends an <a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event, it should send <a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> if any of the following occur:
      

<ul>
<li>The byte stream finishes buffering data.
          </li>
<li>The byte stream reaches the end of the stream.
          </li>
<li>The media source calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>FALSE</b>.
          </li>
<li>The media source calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-stopbuffering">StopBuffering</a>.
          </li>
</ul>
The byte stream should not send any more buffering events after it reaches the end of the file.
      

If buffering is disabled, the byte stream does not send any buffering events. Internally, however, it might still buffer data while it waits for I/O requests to complete. Therefore, <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> methods might take an indefinite length of time to complete.
      

If the byte stream is buffering data internally and the media source calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>TRUE</b>, the byte stream can send <a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> immediately.
      

After the presentation has started, the media source should forward and <a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> and <a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> events that it receives while started. The Media Session will pause the presentation clock while buffering is progress and restart the presentation clock when buffering completes. The media source should only forward these events while the presentation is playing. The purpose of sending these events to the Media Session is to pause the presentation time while the source buffers data.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
