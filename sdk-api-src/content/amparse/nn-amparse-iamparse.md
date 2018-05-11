---
UID: NN:amparse.IAMParse
title: IAMParse
author: windows-driver-content
description: The IAMParse interface sets and retrieves the parse time for an MPEG-2 stream.
old-location: dshow\iamparse.htm
old-project: DirectShow
ms.assetid: c5f3e153-c92f-4cdf-9aae-336b1f3dd8d6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAMParse, IAMParse interface [DirectShow], IAMParse interface [DirectShow],described, IAMParseInterface, amparse/IAMParse, dshow.iamparse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: amparse.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SOCKADDR_IRDA, *PSOCKADDR_IRDA, *LPSOCKADDR_IRDA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMParse
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMParse interface


## -description



The <code>IAMParse</code> interface sets and retrieves the <i>parse time</i> for an MPEG-2 stream. The parse time is a notional time associated with the current position in the stream of bytes supplied to the parser filter. This time is also tied to the origin of the time stamps in that time stamp zero corresponds to parse time zero.

The <a href="https://msdn.microsoft.com/06704a5a-e7ae-4187-ae36-32512d951aaf">MPEG-2 Splitter</a> filter implements this interface. Use this interface to retrieve or set the current stream parse time or to clear the data buffer of its current data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMParse</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMParse</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMParse</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Empties the current file buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce87e39e-1e5d-4098-8431-ea9b3188784e">GetParseTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream parse time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52c53994-7cb7-4f50-a00d-87faa309c717">SetParseTime</a>
</td>
<td align="left" width="63%">
Sets the current stream parse time.

</td>
</tr>
</table> 

