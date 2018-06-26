---
UID: NN:segment.IMSVidGenericSink
title: IMSVidGenericSink
author: windows-sdk-content
description: The IMSVidGenericSink interface represents a generic output device that supports streaming output. It is implemented by the MSVidGenericSink object.
old-location: mstv\imsvidgenericsink.htm
old-project: mstv
ms.assetid: 15181a89-aa64-4ecf-aaf5-4aac36753ddf
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidGenericSink, IMSVidGenericSink interface [Microsoft TV Technologies], IMSVidGenericSink interface [Microsoft TV Technologies],described, IMSVidGenericSinkInterface, mstv.imsvidgenericsink, segment/IMSVidGenericSink
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidGenericSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidGenericSink interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        </div>
<div> </div>


The <b>IMSVidGenericSink</b> interface represents a generic output device that supports streaming output. It is implemented by the <a href="https://msdn.microsoft.com/0a5d0550-6587-4c9b-830e-e998e7678e77">MSVidGenericSink</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGenericSink</b> interface inherits from <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>. <b>IMSVidGenericSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidGenericSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e77f2ee8-081b-4415-87b5-ab27ee0218d2">get_SinkStreams</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9bb76ad-6b10-4a48-9d94-64e6d28a3b9f">put_SinkStreams</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a26dc5-a551-4f97-9dd4-6522a14989a8">SetSinkFilter</a>
</td>
<td align="left" width="63%">
Sets the filter for the sink.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGenericSink)</code>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

