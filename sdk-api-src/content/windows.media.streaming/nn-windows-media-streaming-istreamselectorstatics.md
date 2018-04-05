---
UID: NN:windows.media.streaming.IStreamSelectorStatics
title: IStreamSelectorStatics
author: windows-driver-content
description: Encapsulates the methods needed to asynchronously select a stream.
old-location: mediastreaming\istreamselectorstatics.htm
old-project: mediastreaming
ms.assetid: 746BFF49-C75F-417B-A54A-841A4A0E84C5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IStreamSelectorStatics, IStreamSelectorStatics interface [Media Streaming API], IStreamSelectorStatics interface [Media Streaming API], described, mediastreaming.istreamselectorstatics, windows/IStreamSelectorStatics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: PDF_RENDER_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.media.streaming.h
api_name:
-	IStreamSelectorStatics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IStreamSelectorStatics interface


## -description


Encapsulates the methods needed to asynchronously select a stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamSelectorStatics</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamSelectorStatics</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8C1B6DC6-D85E-406F-B6DA-914DC5269666">GetStreamPropertiesAsync</a>
</td>
<td align="left" width="63%">
When implemented gets the properties of the stream asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DE96557-2CA0-4A88-AFF1-6A5480EEE04D">SelectBestStreamAsync</a>
</td>
<td align="left" width="63%">
When implemented queries asynchronously for the best stream.

</td>
</tr>
</table> 

