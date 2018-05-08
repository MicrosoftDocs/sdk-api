---
UID: NN:shobjidl.IAccessibilityDockingServiceCallback
title: IAccessibilityDockingServiceCallback
author: windows-driver-content
description: Receives Acessibility Window Docking events.
old-location: com\iaccessibilitydockingservicecallback.htm
old-project: com
ms.assetid: D69C8040-AAC4-4149-ACDA-948FDBACAB48
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IAccessibilityDockingServiceCallback, IAccessibilityDockingServiceCallback interface [COM], IAccessibilityDockingServiceCallback interface [COM],described, com.iaccessibilitydockingservicecallback, shobjidl/IAccessibilityDockingServiceCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl.h
api_name:
-	IAccessibilityDockingServiceCallback
-	IAccessibilityDockingServiceCallback.Undocked
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IAccessibilityDockingServiceCallback interface


## -description


Receives Acessibility Window Docking events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibilityDockingServiceCallback</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IAccessibilityDockingServiceCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibilityDockingServiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">Undocked</td>
<td align="left" width="63%">
Undocks the accessibility window so that it will not be automatically moved to its previous location.

</td>
</tr>
</table> 

