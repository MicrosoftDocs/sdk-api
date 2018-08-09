---
UID: NN:strmif.IOverlayNotify2
title: IOverlayNotify2
author: windows-sdk-content
description: The IOverlayNotify2 interface derives from the IOverlayNotify interface.
old-location: dshow\ioverlaynotify2.htm
old-project: DirectShow
ms.assetid: 439b3939-84da-48f5-b2a5-47f68fedef06
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IOverlayNotify2, IOverlayNotify2 interface [DirectShow], IOverlayNotify2 interface [DirectShow],described, IOverlayNotify2Interface, dshow.ioverlaynotify2, strmif/IOverlayNotify2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IOverlayNotify2
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlayNotify2 interface


## -description



The <code>IOverlayNotify2</code> interface derives from the <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> interface. <code>IOverlayNotify2</code> gives asynchronous notifications of changes to the rendering window, identifying changes to the exposed window area. The advise link optionally supports this for the purpose of accepting <a href="https://msdn.microsoft.com/8f32a373-5d98-4491-8bfb-9445cb15ff10">IOverlayNotify2::OnDisplayChange</a> notification.

To get notifications that the exposed window area has changed, decoders that do their own drawing should implement an <code>IOverlayNotify2</code> interface.

The video renderer is the only filter that calls the method on this interface. This is done automatically by the default video renderer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOverlayNotify2</b> interface inherits from <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a>. <b>IOverlayNotify2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOverlayNotify2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f32a373-5d98-4491-8bfb-9445cb15ff10">OnDisplayChange</a>
</td>
<td align="left" width="63%">
Provides notification that the exposed window area has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a>
 

 

