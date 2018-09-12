---
UID: NN:comsvcs.IComExceptionEvents
title: IComExceptionEvents
author: windows-sdk-content
description: Notifies the subscriber when an unhandled exception occurs in the user's code.
old-location: cos\icomexceptionevents.htm
tech.root: cossdk
ms.assetid: e484cad0-3b7e-4822-bbde-c953cb0301ca
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComExceptionEvents, IComExceptionEvents interface [COM+], IComExceptionEvents interface [COM+],described, _dtc_IComExceptionEvents, comsvcs/IComExceptionEvents, cos.icomexceptionevents
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComExceptionEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComExceptionEvents interface


## -description


Notifies the subscriber when an unhandled exception occurs in the user's code. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComExceptionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComExceptionEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComExceptionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/961e3668-a35e-4e65-8477-fd7457ecc6ca">OnExceptionUser</a>
</td>
<td align="left" width="63%">
Generated for transactional components when an unhandled exception occurs in the user's code.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

