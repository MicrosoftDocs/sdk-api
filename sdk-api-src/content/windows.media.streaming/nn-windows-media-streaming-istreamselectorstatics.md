---
UID: NN:windows.media.streaming.IStreamSelectorStatics
title: IStreamSelectorStatics (windows.media.streaming.h)
author: windows-sdk-content
description: Encapsulates the methods needed to asynchronously select a stream.
old-location: mediastreaming\istreamselectorstatics.htm
tech.root: mediastreaming
ms.assetid: 746BFF49-C75F-417B-A54A-841A4A0E84C5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamSelectorStatics, IStreamSelectorStatics interface [Media Streaming API], IStreamSelectorStatics interface [Media Streaming API],described, mediastreaming.istreamselectorstatics, windows/IStreamSelectorStatics
ms.topic: interface
f1_keywords: 
 - "windows.media.streaming/IStreamSelectorStatics"
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - windows.media.streaming.h
api_name:
 - IStreamSelectorStatics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamSelectorStatics interface


## -description


Encapsulates the methods needed to asynchronously select a stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamSelectorStatics</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamSelectorStatics</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamSelectorStatics</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828954(v=vs.85)">GetStreamPropertiesAsync</a>
</td>
<td align="left" width="63%">
When implemented gets the properties of the stream asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828955(v=vs.85)">SelectBestStreamAsync</a>
</td>
<td align="left" width="63%">
When implemented queries asynchronously for the best stream.

</td>
</tr>
</table> 

