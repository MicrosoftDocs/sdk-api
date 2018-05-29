---
UID: NN:comsvcs.IMtsGrp
title: IMtsGrp
author: windows-sdk-content
description: Provides methods for enumerating through running packages.
old-location: cos\imtsgrp.htm
old-project: cossdk
ms.assetid: 976b4f0a-79cb-4b2d-8d69-225230147c53
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMtsGrp, IMtsGrp interface [COM+], IMtsGrp interface [COM+],described, _dtc_IMtsGrp_Interface, comsvcs/IMtsGrp, cos.imtsgrp
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
-	IMtsGrp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsGrp interface


## -description


Provides methods for enumerating through running packages.  The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsGrp</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMtsGrp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMtsGrp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84d1d2e1-ea06-4e3f-81d9-bb2ed02cf021">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of running packages in the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/752bda5e-d3e1-4566-90c3-aaa336479670">Refresh</a>
</td>
<td align="left" width="63%">
Updates the list of <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointers that was populated upon the creation of the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

