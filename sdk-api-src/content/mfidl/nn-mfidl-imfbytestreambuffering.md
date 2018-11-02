---
UID: NN:mfidl.IMFByteStreamBuffering
title: IMFByteStreamBuffering
author: windows-sdk-content
description: Controls how a byte stream buffers data from a network.
old-location: mf\imfbytestreambuffering.htm
tech.root: medfound
ms.assetid: bbf9cdb1-5ec7-498a-aa59-85c24779547e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFByteStreamBuffering, IMFByteStreamBuffering interface [Media Foundation], IMFByteStreamBuffering interface [Media Foundation],described, bbf9cdb1-5ec7-498a-aa59-85c24779547e, mf.imfbytestreambuffering, mfidl/IMFByteStreamBuffering
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamBuffering interface


## -description


Controls how a byte stream buffers data from a network.
        

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamBuffering</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFByteStreamBuffering</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5f7418ff-32e5-49b3-b7b3-6686e6562d51">EnableBuffering</a>
</td>
<td align="left" width="63%">
Enables or disables buffering.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/033ea7d4-d669-497b-be37-a8c9a6584209">SetBufferingParams</a>
</td>
<td align="left" width="63%">
Sets the buffering parameters.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da342ac4-bb61-40d6-9b67-0480ac2a780f">StopBuffering</a>
</td>
<td align="left" width="63%">
Stops any buffering that is in progress.
        

</td>
</tr>
</table> 


## -remarks



If a byte stream implements this interface, a media source can use it to control how the byte stream buffers data. This interface is designed for byte streams that read data from a network.
      

A byte stream that implements this interface should also implement the <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> interface. When the byte stream starts buffering, it sends an <a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a> event. When it stops buffering, it sends an <a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a> event.
      

The byte stream must send a matching <a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a> event for every <a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a> event. The byte stream must not send MEBufferingStarted events unless the media source has enabled buffering by calling <a href="https://msdn.microsoft.com/5f7418ff-32e5-49b3-b7b3-6686e6562d51">EnableBuffering</a> with the value <b>TRUE</b>.
      

After the byte stream sends an <a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a> event, it should send <a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a> if any of the following occur:
      

<ul>
<li>The byte stream finishes buffering data.
          </li>
<li>The byte stream reaches the end of the stream.
          </li>
<li>The media source calls <a href="https://msdn.microsoft.com/5f7418ff-32e5-49b3-b7b3-6686e6562d51">EnableBuffering</a> with the value <b>FALSE</b>.
          </li>
<li>The media source calls <a href="https://msdn.microsoft.com/da342ac4-bb61-40d6-9b67-0480ac2a780f">StopBuffering</a>.
          </li>
</ul>
The byte stream should not send any more buffering events after it reaches the end of the file.
      

If buffering is disabled, the byte stream does not send any buffering events. Internally, however, it might still buffer data while it waits for I/O requests to complete. Therefore, <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> methods might take an indefinite length of time to complete.
      

If the byte stream is buffering data internally and the media source calls <a href="https://msdn.microsoft.com/5f7418ff-32e5-49b3-b7b3-6686e6562d51">EnableBuffering</a> with the value <b>TRUE</b>, the byte stream can send <a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a> immediately.
      

After the presentation has started, the media source should forward and <a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a> and <a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a> events that it receives while started. The Media Session will pause the presentation clock while buffering is progress and restart the presentation clock when buffering completes. The media source should only forward these events while the presentation is playing. The purpose of sending these events to the Media Session is to pause the presentation time while the source buffers data.
      




## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>



<a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

