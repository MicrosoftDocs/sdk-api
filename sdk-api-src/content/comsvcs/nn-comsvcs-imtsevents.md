---
UID: NN:comsvcs.IMtsEvents
title: IMtsEvents
author: windows-sdk-content
description: Provides methods for obtaining information about the running package and establishing event sinks.
old-location: cos\imtsevents.htm
old-project: cossdk
ms.assetid: 7db3a373-00d3-480e-8f8e-7e65a468d5dc
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMtsEvents, IMtsEvents interface [COM+], IMtsEvents interface [COM+],described, _dtc_IMtsEvents_Interface, comsvcs/IMtsEvents, cos.imtsevents
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsEvents interface


## -description


Provides methods for obtaining information about the running package and establishing event sinks. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMtsEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMtsEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fad889d2-412e-4dc7-8380-408bda456037">get_FireEvents</a>
</td>
<td align="left" width="63%">
Retrieves whether events are enabled or disabled for an event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7afd68f7-8aba-4c0f-a262-9a0ea861e063">get_PackageGuid</a>
</td>
<td align="left" width="63%">
Retrieves the globally unique identifier (GUID) for the package in which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b23828f-cadc-472d-9186-0712e0120b60">get_PackageName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the package in which the instance of the object that implements the <b>IMtsEvents</b> interface is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9950eeab-0b90-4810-9163-8c5582d0b748">GetProcessID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the process in which the event occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dcbe3d9-f81b-4014-a3b4-16706e691cb0">PostEvent</a>
</td>
<td align="left" width="63%">
Posts a user-defined event to an event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

