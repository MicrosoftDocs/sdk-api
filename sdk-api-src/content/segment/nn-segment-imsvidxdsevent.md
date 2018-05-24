---
UID: NN:segment.IMSVidXDSEvent
title: IMSVidXDSEvent
author: windows-driver-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidXDSEvent interface is used to receive events from the MSVidXDS object.This interface is an outgoing connection-point interface.
old-location: mstv\imsvidxdsevent.htm
old-project: mstv
ms.assetid: c89f378d-daa6-4e01-a087-6082d368585b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidXDSEvent, IMSVidXDSEvent interface [Microsoft TV Technologies], IMSVidXDSEvent interface [Microsoft TV Technologies],described, IMSVidXDSEventInterface, mstv.imsvidxdsevent, segment/IMSVidXDSEvent
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMSVidXDSEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidXDSEvent interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidXDSEvent</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/30b9709e-8f37-4b74-ad96-6da48efaff32">MSVidXDS</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidXDSEvent</b> interface inherits from <a href="https://msdn.microsoft.com/821a5524-5811-417b-9604-0883315080eb">IMSVidFeatureEvent</a>. <b>IMSVidXDSEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidXDSEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2832f99b-16e9-4c09-903d-8d89f2cc7715">RatingChange</a>
</td>
<td align="left" width="63%">
Called when the current rating changes.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidXDSEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/821a5524-5811-417b-9604-0883315080eb">IMSVidFeatureEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

