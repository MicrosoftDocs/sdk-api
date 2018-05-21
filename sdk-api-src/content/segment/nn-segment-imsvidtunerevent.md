---
UID: NN:segment.IMSVidTunerEvent
title: IMSVidTunerEvent
author: windows-driver-content
description: This topic applies to Windows XP or later.
old-location: mstv\imsvidtunerevent.htm
old-project: mstv
ms.assetid: cdffe6ca-00b0-4230-963d-b4409413e5f5
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidTunerEvent, IMSVidTunerEvent interface [Microsoft TV Technologies], IMSVidTunerEvent interface [Microsoft TV Technologies],described, IMSVidTunerEventInterface, mstv.imsvidtunerevent, segment/IMSVidTunerEvent
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
-	IMSVidTunerEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidTunerEvent interface


## -description



This topic applies to Windows XP or later.
        

The <b>IMSVidTunerEvent</b> interface is used to receive events from BDA-compliant digital TV tuners.

This interface is an outgoing connection-point interface. To receive events from a BDA digital tuner, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="https://msdn.microsoft.com/a29f2bb1-650e-43f8-8949-b3944c54a9e1">MSVidBDATunerDevice</a> object to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidTunerEvent</b> interface inherits from <a href="https://msdn.microsoft.com/9f35953a-3fea-4187-ad14-28f2c8dc2716">IMSVidInputDeviceEvent</a>. <b>IMSVidTunerEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidTunerEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fc30a5a-b934-4c75-9cc8-5a039843ebe8">TuneChanged</a>
</td>
<td align="left" width="63%">
Signals that the tuner has tuned to a new frequency.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTunerEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9f35953a-3fea-4187-ad14-28f2c8dc2716">IMSVidInputDeviceEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

