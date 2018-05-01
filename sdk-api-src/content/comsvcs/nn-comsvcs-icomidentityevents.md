---
UID: NN:comsvcs.IComIdentityEvents
title: IComIdentityEvents
author: windows-driver-content
description: Notifies the subscriber about an activity that is part of an Internet Information Services (IIS) Active Server Pages (ASP) page. For example, if a COM+ object is invoked in an ASP page, the user would be notified of this activity.
old-location: cos\icomidentityevents.htm
old-project: cossdk
ms.assetid: f064a5cd-c84d-4b80-96fc-1036af333901
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComIdentityEvents, IComIdentityEvents interface [COM+], IComIdentityEvents interface [COM+], described, _dtc_IComIdentityEvents, comsvcs/IComIdentityEvents, cos.icomidentityevents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComIdentityEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComIdentityEvents interface


## -description


Notifies the subscriber about an activity that is part of an Internet Information Services (IIS) Active Server Pages (ASP) page. For example, if a COM+ object is invoked in an ASP page, the user would be notified of this activity. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComIdentityEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComIdentityEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComIdentityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88beaef9-d042-4836-8223-6063c87ba06a">OnIISRequestInfo</a>
</td>
<td align="left" width="63%">
Generated when an activity is part of an ASP page.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

