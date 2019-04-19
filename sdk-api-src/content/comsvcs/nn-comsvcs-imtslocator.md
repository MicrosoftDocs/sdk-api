---
UID: NN:comsvcs.IMTSLocator
title: IMTSLocator (comsvcs.h)
author: windows-sdk-content
description: Describes a single event that provides access to the IMtsEvents interface of the event dispatcher for the current process.
old-location: cos\imtslocator.htm
tech.root: cossdk
ms.assetid: afa559bc-5ac2-4487-bb13-25f30c5f4033
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMTSLocator, IMTSLocator interface [COM+], IMTSLocator interface [COM+],described, _dtc_IMtsLocator_Interface, comsvcs/IMTSLocator, cos.imtslocator
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
 - IMTSLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMTSLocator interface


## -description


Describes a single event that provides access to the <a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a> interface of the event dispatcher for the current process. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMTSLocator</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMTSLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMTSLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10e110bf-1a7c-48a2-ab9f-836ea21d442b">GetEventDispatcher</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the event dispatcher for the current process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

