---
UID: NN:tuner.IBroadcastEventEx
title: IBroadcastEventEx
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\ibroadcasteventex.htm
old-project: mstv
ms.assetid: c16ad538-afc6-4530-a2fd-18965b63983b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBroadcastEventEx, IBroadcastEventEx interface [Microsoft TV Technologies], IBroadcastEventEx interface [Microsoft TV Technologies],described, IBroadcastEventExInterface, mstv.ibroadcasteventex, tuner/IBroadcastEventEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IBroadcastEventEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IBroadcastEventEx interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IBroadcastEventEx</b> interface is an extended version of the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface. 

Like <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a>, the <b>IBroadcastEventEx</b> interface enables an object to receive events from another object without setting up a direct connection point. Applications typically do not need to use either of these interfaces.

For information about implementing a class that can source or sink broadcast events, see the example code in <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent Interface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBroadcastEventEx</b> interface inherits from <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a>. <b>IBroadcastEventEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBroadcastEventEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b">FireEx</a>
</td>
<td align="left" width="63%">
Fires an event.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBroadcastEventEx)</code>.




## -see-also




<a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

