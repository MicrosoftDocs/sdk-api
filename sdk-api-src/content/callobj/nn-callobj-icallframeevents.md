---
UID: NN:callobj.ICallFrameEvents
title: ICallFrameEvents
author: windows-driver-content
description: Delivers method call notifications.
old-location: com\icallframeevents.htm
old-project: com
ms.assetid: 2f1e1b8d-6150-45e9-89e2-524d80df558d
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICallFrameEvents, ICallFrameEvents interface [COM], ICallFrameEvents interface [COM],described, _com_icallframeevents_interface, callobj/ICallFrameEvents, com.icallframeevents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CALLFRAME_COPY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Callobj.h
api_name:
-	ICallFrameEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrameEvents interface


## -description


Delivers method call notifications.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrameEvents</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICallFrameEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallFrameEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdccc4a7-e408-4186-8cc0-b14feacfbf04">OnCall</a>
</td>
<td align="left" width="63%">
Informs the event sink if it receives a method call on the interceptor.

</td>
</tr>
</table> 

