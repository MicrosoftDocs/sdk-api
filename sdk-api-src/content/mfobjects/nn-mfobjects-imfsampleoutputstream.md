---
UID: NN:mfobjects.IMFSampleOutputStream
title: IMFSampleOutputStream (mfobjects.h)
author: windows-sdk-content
description: Writes media samples to a byte stream.
old-location: mf\imfsampleoutputstream.htm
tech.root: medfound
ms.assetid: BA293BB7-9191-4123-96DB-FF6386ABB3AE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFSampleOutputStream, IMFSampleOutputStream interface [Media Foundation], IMFSampleOutputStream interface [Media Foundation],described, mf.imfsampleoutputstream, mfobjects/IMFSampleOutputStream
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFSampleOutputStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSampleOutputStream interface


## -description


Writes media samples to a byte stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleOutputStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSampleOutputStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleOutputStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41056795-3E12-448E-9341-FB4DD4E7D079">BeginWriteSample</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to write a media sample to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE65CE63-B7FF-403B-ABB8-5E6C53CAD314">EndWriteSample</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to write a media sample to the stream.

</td>
</tr>
</table> 


## -remarks



A writeable byte stream can optionally implement this interface. 

This interface enables the caller to send media samples to the byte stream for writing, instead of using the <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">IMFByteStream::BeginWrite</a> method to write blobs of untyped data. The byte stream can use the information contained in the media sample to optimize how it writes the data. For example, a byte stream that sends media data over a network can optimize based on the time stamp.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the byte stream object.

Any implementation of <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> that exposes <b>IMFSampleOutputStream</b> as an interface needs to honor the following requirements:

<ul>
<li> All writes from either interface always go to the exact same byte stream object.
</li>
<li>The current position for both <b>IMFSampleOutputStream</b> and <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> shall always be the same. For example, writing to <b>IMFSampleOutputStream</b> will also update the current position of  <b>IMFByteStream</b>.
</li>
<li>Writing a sample using <a href="https://msdn.microsoft.com/41056795-3E12-448E-9341-FB4DD4E7D079">BeginWriteSample</a> and <a href="https://msdn.microsoft.com/AE65CE63-B7FF-403B-ABB8-5E6C53CAD314">EndWriteSample</a> shall serialize the sample by writing the data from all the buffers in the sample, in the order in which the buffers are stored in the sample.  (Use <a href="https://msdn.microsoft.com/48d3b861-96e8-4767-a8b1-65614fd48254">IMFSample::GetBufferByIndex</a> to get the individual buffers by index value.) The total bytes copied shall be the number of bytes written from all the buffers. </li>
</ul>







## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

