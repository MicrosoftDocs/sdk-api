---
UID: NN:comsvcs.IComApp2Events
title: IComApp2Events
author: windows-sdk-content
description: Notifies the subscriber if a COM+ server application is loaded, shut down, or paused.
old-location: cos\icomapp2events.htm
tech.root: cossdk
ms.assetid: 45e0d26b-7485-436b-9b64-fa48217b32d1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComApp2Events, IComApp2Events interface [COM+], IComApp2Events interface [COM+],described, _dtc_icomapp2events, comsvcs/IComApp2Events, cos.icomapp2events
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IComApp2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComApp2Events interface


## -description


Notifies the subscriber if a COM+ server application is loaded, shut down, or paused. The subscriber is also notified if the application is marked for recycling. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComApp2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComApp2Events</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IComApp2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686803(v=VS.85).aspx">OnAppActivation2</a>
</td>
<td align="left" width="63%">
Generated when the server application process is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682793(v=VS.85).aspx">OnAppForceShutdown2</a>
</td>
<td align="left" width="63%">
Generated when the server application is forced to shut down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678853(v=VS.85).aspx">OnAppPaused2</a>
</td>
<td align="left" width="63%">
Generated when the server application is paused or resumed to its initial state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679844(v=VS.85).aspx">OnAppRecycle2</a>
</td>
<td align="left" width="63%">
Generated when the server application process is marked for recycling termination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685097(v=VS.85).aspx">OnAppShutdown2</a>
</td>
<td align="left" width="63%">
Generated when the server application shuts down.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

