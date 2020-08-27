---
UID: NN:mfobjects.IMFByteStream
title: IMFByteStream (mfobjects.h)
description: Represents a byte stream from some data source, which might be a local file, a network file, or some other source.
helpviewer_keywords: ["690035b7-2855-4714-938f-f8250ec70d24","IMFByteStream","IMFByteStream interface [Media Foundation]","IMFByteStream interface [Media Foundation]","described","mf.imfbytestream","mfobjects/IMFByteStream"]
old-location: mf\imfbytestream.htm
tech.root: mf
ms.assetid: 690035b7-2855-4714-938f-f8250ec70d24
ms.date: 12/05/2018
ms.keywords: 690035b7-2855-4714-938f-f8250ec70d24, IMFByteStream, IMFByteStream interface [Media Foundation], IMFByteStream interface [Media Foundation],described, mf.imfbytestream, mfobjects/IMFByteStream
f1_keywords:
- mfobjects/IMFByteStream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStream interface


## -description


Represents a byte stream from some data source, which might be a local file, a network file, or some other source. The <b>IMFByteStream</b> interface supports the typical stream operations, such as reading, writing, and seeking.
        
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread">BeginRead</a>
</td>
<td align="left" width="63%">
Begins an asynchronous read operation from the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>
</td>
<td align="left" width="63%">
Begins an asynchronous write operation to the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-close">Close</a>
</td>
<td align="left" width="63%">
Closes the stream and releases any resources associated with the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread">EndRead</a>
</td>
<td align="left" width="63%">
Completes an asynchronous read operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endwrite">EndWrite</a>
</td>
<td align="left" width="63%">
Completes an asynchronous write operation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-flush">Flush</a>
</td>
<td align="left" width="63%">
Clears any internal buffers used by the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the byte stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcurrentposition">GetCurrentPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current read or write position in the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream">IsEndOfStream</a>
</td>
<td align="left" width="63%">
Queries whether the current position has reached the end of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read">Read</a>
</td>
<td align="left" width="63%">
Reads data from the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>
</td>
<td align="left" width="63%">
Moves the current position in the stream by a specified offset.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>
</td>
<td align="left" width="63%">
Sets the current read or write position.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setlength">SetLength</a>
</td>
<td align="left" width="63%">
Sets the length of the stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile">MFCreateFile</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile">MFCreateTempFile</a>
</li>
</ul>
A byte stream for a media souce can be opened with read access. A byte stream for an archive media sink should be opened with both read and write access. (Read access may be required, because the archive sink might need to read portions of the file as it writes.)
      

Some implementations of this interface also expose one or more of the following interfaces:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>
</li>
</ul>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/byte-stream-attributes">Byte Stream Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

