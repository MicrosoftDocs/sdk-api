---
UID: NN:comsvcs.IMtsEventInfo
title: IMtsEventInfo
author: windows-sdk-content
description: Describes user-defined events.
old-location: cos\imtseventinfo.htm
old-project: cossdk
ms.assetid: 9508df6d-281b-4a02-bb95-233b369b8279
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMtsEventInfo, IMtsEventInfo interface [COM+], IMtsEventInfo interface [COM+],described, _dtc_IMtsEventInfo_Interface, comsvcs/IMtsEventInfo, cos.imtseventinfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMtsEventInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsEventInfo interface


## -description


Describes user-defined events. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsEventInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMtsEventInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMtsEventInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f92c93eb-841a-4bc8-9c02-644c30daccad">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of data values from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3d8ed52-0ad3-4073-877b-071bac90c71f">get_DisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20695360-ed0d-4d8b-8c3b-42adc42e87b3">get_EventID</a>
</td>
<td align="left" width="63%">
Retrieves the event identifier of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83ce3935-2c9a-4ebe-8758-9ac349d4a73b">get_Names</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the names of the data values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61757e85-28b2-4599-9be4-69a3531e5ac2">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified user-defined event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

