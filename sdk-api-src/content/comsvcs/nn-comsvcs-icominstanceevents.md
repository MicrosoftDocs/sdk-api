---
UID: NN:comsvcs.IComInstanceEvents
title: IComInstanceEvents (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber of an object's creation or release.
old-location: cos\icominstanceevents.htm
tech.root: cossdk
ms.assetid: 11e4559e-04c5-4fa9-b618-458ca7daf00e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComInstanceEvents, IComInstanceEvents interface [COM+], IComInstanceEvents interface [COM+],described, _dtc_IComInstanceEvents, comsvcs/IComInstanceEvents, cos.icominstanceevents
ms.topic: interface
f1_keywords: 
 - "comsvcs/IComInstanceEvents"
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
 - IComInstanceEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComInstanceEvents interface


## -description


Notifies the subscriber of an object's creation or release. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComInstanceEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComInstanceEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComInstanceEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icominstanceevents-onobjectcreate">OnObjectCreate</a>
</td>
<td align="left" width="63%">
Generated when an object is created by a client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icominstanceevents-onobjectdestroy">OnObjectDestroy</a>
</td>
<td align="left" width="63%">
Generated when an object is released by a client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

