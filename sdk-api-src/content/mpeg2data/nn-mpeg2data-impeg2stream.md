---
UID: NN:mpeg2data.IMpeg2Stream
title: IMpeg2Stream (mpeg2data.h)
author: windows-sdk-content
description: The IMpeg2Stream interface represents a stream of MPEG-2 data. The IMpeg2Data::GetStreamOfSections method returns a pointer to this interface.
old-location: mstv\impeg2stream.htm
tech.root: mstv
ms.assetid: 189c921a-ec49-48dc-8c60-3d3ec2a648ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMpeg2Stream, IMpeg2Stream interface [Microsoft TV Technologies], IMpeg2Stream interface [Microsoft TV Technologies],described, IMpeg2StreamInterface, mpeg2data/IMpeg2Stream, mstv.impeg2stream
ms.topic: interface
req.header: mpeg2data.h
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
 - Mpeg2data.h
api_name:
 - IMpeg2Stream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpeg2Stream interface


## -description



The <b>IMpeg2Stream</b> interface represents a stream of MPEG-2 data. The <a href="https://msdn.microsoft.com/896080ff-cdf0-40b1-ba4e-d94de527d86e">IMpeg2Data::GetStreamOfSections</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2Stream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMpeg2Stream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMpeg2Stream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2ef2ebc-55dc-49d4-a5de-18203de113ce">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68950eba-6c23-49f7-9651-d4db9e554de3">SupplyDataBuffer</a>
</td>
<td align="left" width="63%">
Provides a buffer for the object to write data.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2Stream)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

