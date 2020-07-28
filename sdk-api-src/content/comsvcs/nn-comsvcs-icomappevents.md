---
UID: NN:comsvcs.IComAppEvents
title: IComAppEvents (comsvcs.h)
description: Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.
helpviewer_keywords: ["IComAppEvents","IComAppEvents interface [COM+]","IComAppEvents interface [COM+]","described","_dtc_IComAppEvents","comsvcs/IComAppEvents","cos.icomappevents"]
old-location: cos\icomappevents.htm
tech.root: cos
ms.assetid: 61ae1926-601b-4d97-80e4-d2d2098ced39
ms.date: 12/05/2018
ms.keywords: IComAppEvents, IComAppEvents interface [COM+], IComAppEvents interface [COM+],described, _dtc_IComAppEvents, comsvcs/IComAppEvents, cos.icomappevents
f1_keywords:
- comsvcs/IComAppEvents
dev_langs:
- c++
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
- IComAppEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComAppEvents interface


## -description


Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.  The latter is initiated by the user calling a catalog method, such as <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog-shutdownapplication">ICOMAdminCatalog::ShutdownApplication</a>, to shut down the server. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComAppEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComAppEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomappevents-onappactivation">OnAppActivation</a>
</td>
<td align="left" width="63%">
Generated when an application server starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomappevents-onappforceshutdown">OnAppForceShutdown</a>
</td>
<td align="left" width="63%">
Generated when an application server is forced to shut down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomappevents-onappshutdown">OnAppShutdown</a>
</td>
<td align="left" width="63%">
Generated when an application server shuts down.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

