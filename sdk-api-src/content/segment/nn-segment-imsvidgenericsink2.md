---
UID: NN:segment.IMSVidGenericSink2
title: IMSVidGenericSink2
author: windows-sdk-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidGenericSink2 interface represents a generic output device that supports streaming output. It is implemented by the MSVidGenericSink object.
old-location: mstv\imsvidgenericsink2.htm
old-project: mstv
ms.assetid: 01acd28b-a17a-413a-ab43-9656e3ab7f60
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidGenericSink2, IMSVidGenericSink2 interface [Microsoft TV Technologies], IMSVidGenericSink2 interface [Microsoft TV Technologies],described, IMSVidGenericSink2Interface, mstv.imsvidgenericsink2, segment/IMSVidGenericSink2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidGenericSink2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidGenericSink2 interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidGenericSink2</b> interface represents a generic output device that supports streaming output. It is implemented by the <a href="https://msdn.microsoft.com/0a5d0550-6587-4c9b-830e-e998e7678e77">MSVidGenericSink</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGenericSink2</b> interface inherits from <a href="https://msdn.microsoft.com/15181a89-aa64-4ecf-aaf5-4aac36753ddf">IMSVidGenericSink</a>. <b>IMSVidGenericSink2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b0044995-5bca-4f49-a22b-00df8f73b47f">AddFilter</a>
</td>
<td align="left" width="63%">
Specifies a DirectShow filter that is added to the graph when this segment is built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc899c48-703a-4bdc-849e-73633ae748d0">ResetFilterList</a>
</td>
<td align="left" width="63%">
Clears the list of filters that were added using <a href="https://msdn.microsoft.com/b0044995-5bca-4f49-a22b-00df8f73b47f">AddFilter</a>.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGenericSink2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/15181a89-aa64-4ecf-aaf5-4aac36753ddf">IMSVidGenericSink</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

