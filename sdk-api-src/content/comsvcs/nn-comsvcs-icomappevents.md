---
UID: NN:comsvcs.IComAppEvents
title: IComAppEvents
author: windows-sdk-content
description: Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.
old-location: cos\icomappevents.htm
old-project: cossdk
ms.assetid: 61ae1926-601b-4d97-80e4-d2d2098ced39
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComAppEvents, IComAppEvents interface [COM+], IComAppEvents interface [COM+],described, _dtc_IComAppEvents, comsvcs/IComAppEvents, cos.icomappevents
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComAppEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComAppEvents interface


## -description


Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.  The latter is initiated by the user calling a catalog method, such as <a href="https://msdn.microsoft.com/79f3af18-0924-4e09-85aa-54a6886b65b3">ICOMAdminCatalog::ShutdownApplication</a>, to shut down the server. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComAppEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComAppEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComAppEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4561d15a-6c1b-48e7-9697-87dfb51f877c">OnAppActivation</a>
</td>
<td align="left" width="63%">
Generated when an application server starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7e845fc-be7f-484f-88b9-78206598b57d">OnAppForceShutdown</a>
</td>
<td align="left" width="63%">
Generated when an application server is forced to shut down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4e35147-48c4-4c77-a648-ffd317aa7861">OnAppShutdown</a>
</td>
<td align="left" width="63%">
Generated when an application server shuts down.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

