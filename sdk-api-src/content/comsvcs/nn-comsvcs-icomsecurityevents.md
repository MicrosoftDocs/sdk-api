---
UID: NN:comsvcs.IComSecurityEvents
title: IComSecurityEvents
author: windows-sdk-content
description: Notifies the subscriber if the authentication of a method call succeeded or failed.
old-location: cos\icomsecurityevents.htm
old-project: cossdk
ms.assetid: 83366f18-8dd4-4c3d-8362-4fbcc4c33b95
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IComSecurityEvents, IComSecurityEvents interface [COM+], IComSecurityEvents interface [COM+],described, _dtc_IComSecurityEvents, comsvcs/IComSecurityEvents, cos.icomsecurityevents
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
 - IComSecurityEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComSecurityEvents interface


## -description


Notifies the subscriber if the authentication of a method call succeeded or failed. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComSecurityEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComSecurityEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComSecurityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4be635c6-9601-419d-933e-555b2ae6b73d">OnAuthenticate</a>
</td>
<td align="left" width="63%">
Generated when a method call level authentication succeeds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ead4865-924c-40fb-9ed8-5b98c603c5cf">OnAuthenticateFail</a>
</td>
<td align="left" width="63%">
Generated when a method call level authentication fails.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

