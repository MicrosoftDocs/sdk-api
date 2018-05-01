---
UID: NN:micaut._IMathInputControlEvents
title: "_IMathInputControlEvents"
author: windows-driver-content
description: Exposes the math input control event handlers.
old-location: tablet\_imathinputcontrolevents.htm
old-project: tablet
ms.assetid: e055ab45-53a8-4795-aff6-72987faad5ef
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "_IMathInputControlEvents, _IMathInputControlEvents interface [Tablet PC], _IMathInputControlEvents interface [Tablet PC], described, micaut/_IMathInputControlEvents, tablet._imathinputcontrolevents"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: micaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	micaut.h
api_name:
-	_IMathInputControlEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _IMathInputControlEvents interface


## -description


The <b>_IMathInputControlEvents</b> interface exposes the math input control event handlers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">_IMathInputControlEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>_IMathInputControlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>_IMathInputControlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Clear</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Close</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1d23958-a895-4dfb-ba90-ef5a4913ad7c">Insert</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the <b>Insert</b> button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7a96c34-3f80-451f-88ba-f49de8acd0f1">Paint</a>
</td>
<td align="left" width="63%">
Notifies the event handler when the buttons and background of the control require painting.

</td>
</tr>
</table> 

