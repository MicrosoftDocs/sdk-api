---
UID: NN:comsvcs.ISystemAppEventData
title: ISystemAppEventData
author: windows-sdk-content
description: Notifies the subscriber when a COM+ application instance is created or reconfigured.
old-location: cos\isystemappeventdata.htm
old-project: cossdk
ms.assetid: fd88641e-e0ce-44b7-b8b6-59791be48026
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISystemAppEventData, ISystemAppEventData interface [COM+], ISystemAppEventData interface [COM+],described, _dtc_ISystemAppEventData, comsvcs/ISystemAppEventData, cos.isystemappeventdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - ISystemAppEventData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISystemAppEventData interface


## -description


Notifies the subscriber when a COM+ application instance is created or reconfigured. The application event is published to the subscriber by using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISystemAppEventData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISystemAppEventData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISystemAppEventData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db30c40e-8dd8-4055-b2c4-71f9d0c2efc4">OnDataChanged</a>
</td>
<td align="left" width="63%">
Generated when the configuration of a COM+ application instance is changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89a5adc2-ee65-477d-9247-f075c63b43c7">Startup</a>
</td>
<td align="left" width="63%">
Invoked when a COM+ application instance is created.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

