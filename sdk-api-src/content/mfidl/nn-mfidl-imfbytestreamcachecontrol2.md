---
UID: NN:mfidl.IMFByteStreamCacheControl2
title: IMFByteStreamCacheControl2 (mfidl.h)
description: Controls how a network byte stream transfers data to a local cache.
old-location: mf\imfbytestreamcachecontrol2.htm
tech.root: medfound
ms.assetid: A901F679-B6F2-4DB7-8EFC-EA61249B64FB
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl2, IMFByteStreamCacheControl2 interface [Media Foundation], IMFByteStreamCacheControl2 interface [Media Foundation],described, mf.imfbytestreamcachecontrol2, mfidl/IMFByteStreamCacheControl2
f1_keywords:
- mfidl/IMFByteStreamCacheControl2
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
- IMFByteStreamCacheControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamCacheControl2 interface


## -description


Controls how a network byte stream transfers data to a local cache. This interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamCacheControl2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>. <b>IMFByteStreamCacheControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamCacheControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol2-getbyteranges">GetByteRanges</a>
</td>
<td align="left" width="63%">
Gets the ranges of bytes that are currently stored in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol2-isbackgroundtransferactive">IsBackgroundTransferActive</a>
</td>
<td align="left" width="63%">
Queries whether background transfer is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol2-setcachelimit">SetCacheLimit</a>
</td>
<td align="left" width="63%">
Limits the cache size.

</td>
</tr>
</table> 


## -remarks



Byte streams object in Microsoft Media Foundation can optionally implement this interface. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the byte stream object. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

