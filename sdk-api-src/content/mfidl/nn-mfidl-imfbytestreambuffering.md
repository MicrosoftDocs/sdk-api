---
UID: NN:mfidl.IMFByteStreamBuffering
title: IMFByteStreamBuffering (mfidl.h)

description: Controls how a byte stream buffers data from a network.
old-location: mf\imfbytestreambuffering.htm
tech.root: medfound
ms.assetid: bbf9cdb1-5ec7-498a-aa59-85c24779547e

ms.date: 12/05/2018
ms.keywords: IMFByteStreamBuffering, IMFByteStreamBuffering interface [Media Foundation], IMFByteStreamBuffering interface [Media Foundation],described, bbf9cdb1-5ec7-498a-aa59-85c24779547e, mf.imfbytestreambuffering, mfidl/IMFByteStreamBuffering
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFByteStreamBuffering"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamBuffering interface


## -description


Controls how a byte stream buffers data from a network.
        

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamBuffering</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamBuffering</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamBuffering</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a>
</td>
<td align="left" width="63%">
Enables or disables buffering.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-setbufferingparams">SetBufferingParams</a>
</td>
<td align="left" width="63%">
Sets the buffering parameters.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-stopbuffering">StopBuffering</a>
</td>
<td align="left" width="63%">
Stops any buffering that is in progress.
        

</td>
</tr>
</table> 


## -remarks



If a byte stream implements this interface, a media source can use it to control how the byte stream buffers data. This interface is designed for byte streams that read data from a network.
      

A byte stream that implements this interface should also implement the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface. When the byte stream starts buffering, it sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event. When it stops buffering, it sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> event.
      

The byte stream must send a matching <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> event for every <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event. The byte stream must not send MEBufferingStarted events unless the media source has enabled buffering by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>TRUE</b>.
      

After the byte stream sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> event, it should send <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> if any of the following occur:
      

<ul>
<li>The byte stream finishes buffering data.
          </li>
<li>The byte stream reaches the end of the stream.
          </li>
<li>The media source calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>FALSE</b>.
          </li>
<li>The media source calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-stopbuffering">StopBuffering</a>.
          </li>
</ul>
The byte stream should not send any more buffering events after it reaches the end of the file.
      

If buffering is disabled, the byte stream does not send any buffering events. Internally, however, it might still buffer data while it waits for I/O requests to complete. Therefore, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> methods might take an indefinite length of time to complete.
      

If the byte stream is buffering data internally and the media source calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">EnableBuffering</a> with the value <b>TRUE</b>, the byte stream can send <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> immediately.
      

After the presentation has started, the media source should forward and <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a> and <a href="https://docs.microsoft.com/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> events that it receives while started. The Media Session will pause the presentation clock while buffering is progress and restart the presentation clock when buffering completes. The media source should only forward these events while the presentation is playing. The purpose of sending these events to the Media Session is to pause the presentation time while the source buffers data.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

