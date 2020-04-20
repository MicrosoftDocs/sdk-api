---
UID: NN:mpeg2data.IMpeg2Stream
title: IMpeg2Stream (mpeg2data.h)
description: The IMpeg2Stream interface represents a stream of MPEG-2 data. The IMpeg2Data::GetStreamOfSections method returns a pointer to this interface.helpviewer_keywords: ["IMpeg2Stream","IMpeg2Stream interface [Microsoft TV Technologies]","IMpeg2Stream interface [Microsoft TV Technologies]","described","IMpeg2StreamInterface","mpeg2data/IMpeg2Stream","mstv.impeg2stream"]
old-location: mstv\impeg2stream.htm
tech.root: mstv
ms.assetid: 189c921a-ec49-48dc-8c60-3d3ec2a648ca
ms.date: 12/05/2018
ms.keywords: IMpeg2Stream, IMpeg2Stream interface [Microsoft TV Technologies], IMpeg2Stream interface [Microsoft TV Technologies],described, IMpeg2StreamInterface, mpeg2data/IMpeg2Stream, mstv.impeg2stream
f1_keywords:
- mpeg2data/IMpeg2Stream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpeg2Stream interface


## -description



The <b>IMpeg2Stream</b> interface represents a stream of MPEG-2 data. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getstreamofsections">IMpeg2Data::GetStreamOfSections</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2Stream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2Stream</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2stream-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2stream-supplydatabuffer">SupplyDataBuffer</a>
</td>
<td align="left" width="63%">
Provides a buffer for the object to write data.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2Stream)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

