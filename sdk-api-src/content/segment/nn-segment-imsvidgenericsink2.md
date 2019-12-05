---
UID: NN:segment.IMSVidGenericSink2
title: IMSVidGenericSink2 (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidGenericSink2 interface represents a generic output device that supports streaming output. It is implemented by the MSVidGenericSink object.
old-location: mstv\imsvidgenericsink2.htm
tech.root: mstv
ms.assetid: 01acd28b-a17a-413a-ab43-9656e3ab7f60
ms.date: 12/05/2018
ms.keywords: IMSVidGenericSink2, IMSVidGenericSink2 interface [Microsoft TV Technologies], IMSVidGenericSink2 interface [Microsoft TV Technologies],described, IMSVidGenericSink2Interface, mstv.imsvidgenericsink2, segment/IMSVidGenericSink2
ms.topic: interface
f1_keywords:
- segment/IMSVidGenericSink2
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- segment.h
api_name:
- IMSVidGenericSink2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidGenericSink2 interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidGenericSink2</b> interface represents a generic output device that supports streaming output. It is implemented by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695128(v=vs.85)">MSVidGenericSink</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGenericSink2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidgenericsink">IMSVidGenericSink</a>. <b>IMSVidGenericSink2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidGenericSink2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink2-addfilter">AddFilter</a>
</td>
<td align="left" width="63%">
Specifies a DirectShow filter that is added to the graph when this segment is built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink2-resetfilterlist">ResetFilterList</a>
</td>
<td align="left" width="63%">
Clears the list of filters that were added using <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink2-addfilter">AddFilter</a>.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGenericSink2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidgenericsink">IMSVidGenericSink</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

