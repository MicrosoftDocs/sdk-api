---
UID: NN:mfidl.IMFByteStreamHandler
title: IMFByteStreamHandler (mfidl.h)
author: windows-sdk-content
description: Creates a media source from a byte stream.
old-location: mf\imfbytestreamhandler.htm
tech.root: medfound
ms.assetid: 80c402d4-8246-42ee-a981-69c8d605cb0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 80c402d4-8246-42ee-a981-69c8d605cb0f, IMFByteStreamHandler, IMFByteStreamHandler interface [Media Foundation], IMFByteStreamHandler interface [Media Foundation],described, mf.imfbytestreamhandler, mfidl/IMFByteStreamHandler
ms.topic: interface
f1_keywords: ["mfidl/IMFByteStreamHandler"]
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
 - IMFByteStreamHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamHandler interface


## -description


Creates a media source from a byte stream.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject">BeginCreateObject</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create a media source from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation">CancelObjectCreation</a>
</td>
<td align="left" width="63%">
Cancels the current request to create a media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject">EndCreateObject</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create a media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution">GetMaxNumberOfBytesRequiredForResolution</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of bytes needed to create the media source or determine that the byte stream handler cannot parse this stream.

</td>
</tr>
</table> 


## -remarks



Applications do not use this interface directly. This interface is exposed by byte-stream handlers, which are used by the source resolver. When the byte-stream handler is given a byte stream, it parses the stream and creates a media source. Byte-stream handlers are registered by file name extension or MIME type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
 

 

