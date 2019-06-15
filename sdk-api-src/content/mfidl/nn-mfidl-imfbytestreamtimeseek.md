---
UID: NN:mfidl.IMFByteStreamTimeSeek
title: IMFByteStreamTimeSeek (mfidl.h)
author: windows-sdk-content
description: Seeks a byte stream by time position.
old-location: mf\imfbytestreamtimeseek.htm
tech.root: medfound
ms.assetid: BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFByteStreamTimeSeek, IMFByteStreamTimeSeek interface [Media Foundation], IMFByteStreamTimeSeek interface [Media Foundation],described, mf.imfbytestreamtimeseek, mfidl/IMFByteStreamTimeSeek
ms.topic: interface
req.header: mfidl.h
req.include-header: 
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
 - mfidl.h
api_name:
 - IMFByteStreamTimeSeek
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamTimeSeek interface


## -description


Seeks a byte stream by time position.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamTimeSeek</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamTimeSeek</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamTimeSeek</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamtimeseek-gettimeseekresult">GetTimeSeekResult</a>
</td>
<td align="left" width="63%">
Gets the result of a time-based seek.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamtimeseek-istimeseeksupported">IsTimeSeekSupported</a>
</td>
<td align="left" width="63%">
Queries whether the byte stream supports time-based seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamtimeseek-timeseek">TimeSeek</a>
</td>
<td align="left" width="63%">
Seeks to a new position in the byte stream.

</td>
</tr>
</table> 


## -remarks



A byte stream can implement this interface if it supports time-based seeking. For example, a byte stream that reads data from a server  might implement the interface. Typically, a local file-based byte stream would not implement it.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the byte stream object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

