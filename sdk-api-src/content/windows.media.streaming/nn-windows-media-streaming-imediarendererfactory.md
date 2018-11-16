---
UID: NN:windows.media.streaming.IMediaRendererFactory
title: IMediaRendererFactory
author: windows-sdk-content
description: Encapsulates the methods needed to asynchronously create a new instance of an object that implements the IMediaRenderer interface.
old-location: mediastreaming\imediarendererfactory.htm
tech.root: mediastreaming
ms.assetid: E07EC208-CF00-46D0-B00D-AA8E59F12A0A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMediaRendererFactory, IMediaRendererFactory interface [Media Streaming API], IMediaRendererFactory interface [Media Streaming API],described, mediastreaming.imediarendererfactory, windows/IMediaRendererFactory
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
 - IMediaRendererFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRendererFactory interface


## -description


Encapsulates the methods needed to asynchronously create a new instance of an object that implements the <a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRendererFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaRendererFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaRendererFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD1242F8-4C2E-4027-B1DE-5FD69557684C">CreateMediaRendererAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a new instance of an object that implements the <a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a> interface using the specified Unique Device Name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14A83789-0F3C-467B-8EFD-3BB421C54217">CreateMediaRendererFromBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a new instance of an object that implements the <a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a> interface using the specified <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a> interface.

</td>
</tr>
</table> 

