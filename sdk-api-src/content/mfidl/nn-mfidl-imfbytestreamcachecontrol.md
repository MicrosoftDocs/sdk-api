---
UID: NN:mfidl.IMFByteStreamCacheControl
title: IMFByteStreamCacheControl (mfidl.h)
author: windows-sdk-content
description: Controls how a network byte stream transfers data to a local cache.
old-location: mf\imfbytestreamcachecontrol.htm
tech.root: medfound
ms.assetid: e12a532a-4624-4e06-8e19-6e9daec550ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl, IMFByteStreamCacheControl interface [Media Foundation], IMFByteStreamCacheControl interface [Media Foundation],described, mf.imfbytestreamcachecontrol, mfidl/IMFByteStreamCacheControl
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStreamCacheControl interface


## -description


Controls how a network byte stream transfers data to a local cache. Optionally, this interface is exposed by byte streams that read data from a network, for example, through HTTP.
      

To get a pointer to this interface, call <b>QueryInterface</b> on the byte stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamCacheControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFByteStreamCacheControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamCacheControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol-stopbackgroundtransfer">StopBackgroundTransfer</a>
</td>
<td align="left" width="63%">
Stops the background transfer of data to the local cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

