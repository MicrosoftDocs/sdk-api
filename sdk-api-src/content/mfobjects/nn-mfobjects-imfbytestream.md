---
UID: NN:mfobjects.IMFByteStream
title: IMFByteStream (mfobjects.h)
author: windows-sdk-content
description: Represents a byte stream from some data source, which might be a local file, a network file, or some other source.
old-location: mf\imfbytestream.htm
tech.root: medfound
ms.assetid: 690035b7-2855-4714-938f-f8250ec70d24
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 690035b7-2855-4714-938f-f8250ec70d24, IMFByteStream, IMFByteStream interface [Media Foundation], IMFByteStream interface [Media Foundation],described, mf.imfbytestream, mfobjects/IMFByteStream
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFByteStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStream interface


## -description


Represents a byte stream from some data source, which might be a local file, a network file, or some other source. The <b>IMFByteStream</b> interface supports the typical stream operations, such as reading, writing, and seeking.
        
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFByteStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed4aaf2a-270c-4518-b04d-cdac966bf9a5">BeginRead</a>
</td>
<td align="left" width="63%">
Begins an asynchronous read operation from the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>
</td>
<td align="left" width="63%">
Begins an asynchronous write operation to the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5f704ab-fa3f-4a53-9b97-eb48a75e481b">Close</a>
</td>
<td align="left" width="63%">
Closes the stream and releases any resources associated with the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd62f644-fb97-474b-8303-3086a7b51c4d">EndRead</a>
</td>
<td align="left" width="63%">
Completes an asynchronous read operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3e10e89-ef5d-41c5-b549-4bd632d9370d">EndWrite</a>
</td>
<td align="left" width="63%">
Completes an asynchronous write operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ea6c38-52f3-405e-8a8f-be5d0527099c">Flush</a>
</td>
<td align="left" width="63%">
Clears any internal buffers used by the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/715e802b-4707-4c6d-9ae9-a4ddfa90f05e">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the byte stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de36742a-a8a5-4f40-9fea-af89d9a6bf2e">GetCurrentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current read or write position in the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fb817a6-5b43-4716-a997-bbd8a0b9305d">GetLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e5c02ea-d3fc-4d8d-aa8b-87aa033a3644">IsEndOfStream</a>
</td>
<td align="left" width="63%">
Queries whether the current position has reached the end of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e0d5363-f2c2-4334-86ca-71fac61073d3">Read</a>
</td>
<td align="left" width="63%">
Reads data from the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/512c67a5-e87d-4a81-8577-e64dac868c40">Seek</a>
</td>
<td align="left" width="63%">
Moves the current position in the stream by a specified offset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>
</td>
<td align="left" width="63%">
Sets the current read or write position.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55bee595-0a32-4b9e-8b22-48fdb2913dfc">SetLength</a>
</td>
<td align="left" width="63%">
Sets the length of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1f1195a-b6ee-441c-af8b-fce3dc163e95">Write</a>
</td>
<td align="left" width="63%">
Writes data to the stream.
        

</td>
</tr>
</table> 


## -remarks



The following functions return <b>IMFByteStream</b> pointers for local files:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29269ea4-151f-4819-ae49-9f1c13a901e5">MFCreateFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678">MFCreateTempFile</a>
</li>
</ul>
A byte stream for a media souce can be opened with read access. A byte stream for an archive media sink should be opened with both read and write access. (Read access may be required, because the archive sink might need to read portions of the file as it writes.)
      

Some implementations of this interface also expose one or more of the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/102a1dff-8419-4f86-a145-53ce3d0123f5">IMFGetService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>
</li>
</ul>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6">Byte Stream Attributes</a>



<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

