---
UID: NN:strmif.IAMAsyncReaderTimestampScaling
title: IAMAsyncReaderTimestampScaling
author: windows-sdk-content
description: Enables a pull-mode source filter to support larger file sizes.
old-location: dshow\iamasyncreadertimestampscaling.htm
old-project: DirectShow
ms.assetid: 159ed107-383d-4a1a-b172-f2e339d6bc83
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMAsyncReaderTimestampScaling, IAMAsyncReaderTimestampScaling interface [DirectShow], IAMAsyncReaderTimestampScaling interface [DirectShow],described, dshow.iamasyncreadertimestampscaling, strmif/IAMAsyncReaderTimestampScaling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAsyncReaderTimestampScaling
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAsyncReaderTimestampScaling interface


## -description


Enables a pull-mode source filter to support larger file sizes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMAsyncReaderTimestampScaling</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMAsyncReaderTimestampScaling</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMAsyncReaderTimestampScaling</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fbadd9d-e741-482f-9ff1-655b149fec49">GetTimestampMode</a>
</td>
<td align="left" width="63%">
Gets the filter's time-stamping mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f556e26-049d-4024-95a2-c899be1ef180">SetTimestampMode</a>
</td>
<td align="left" width="63%">
Sets the filter's time-stamping mode.

</td>
</tr>
</table> 


## -remarks



In the pull model, the parser filter requests data from the source filter by calling <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a>. The input to this method is a media sample. The time stamp on the sample specifies the location to read in the stream, as a byte offset.

By default, the time stamp uses the following formula: Time = byte offset × 10000000. This scaling factor limits the effective file size to about 860 GB. To support larger file sizes, call <a href="https://msdn.microsoft.com/7f556e26-049d-4024-95a2-c899be1ef180">SetTimestampMode</a> with the value <b>TRUE</b>. This call sets the scaling factor to 1, so the formula becomes: Time = byte offset.




## -see-also




<a href="https://msdn.microsoft.com/b5246dfe-e6ee-4b91-bfe3-2ec8b8723938">Pull Model</a>
 

 

