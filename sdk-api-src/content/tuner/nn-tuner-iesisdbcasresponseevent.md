---
UID: NN:tuner.IESIsdbCasResponseEvent
title: IESIsdbCasResponseEvent
author: windows-sdk-content
description: Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) IsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent.htm
old-project: mstv
ms.assetid: 141c6798-5dca-495e-bdbe-f07e457a3d8a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IESIsdbCasResponseEvent, IESIsdbCasResponseEvent interface [DirectShow], IESIsdbCasResponseEvent interface [DirectShow],described, mstv.iesisdbcasresponseevent, tuner/IESIsdbCasResponseEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESIsdbCasResponseEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESIsdbCasResponseEvent interface


## -description


Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) <b>IsdbCasResponse</b> event. An Integrated Services Digital Broadcasting (ISDB) PBDA media transform device (MTD) fires an <b>IsdbCasResponse</b> event after a media sink device (MSD)  calls the <a href="https://msdn.microsoft.com/c93351f5-1829-4405-b665-00f2e78391e0">IBDA_ISDBConditionalAccess::SetIsdbCasRequest</a> method to indicate communication with a conditional access system (CAS) card. The MTD fires the <b>IsdbCasResponse</b> event to signal that response data is available.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESIsdbCasResponseEvent</b> interface inherits from <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>. <b>IESIsdbCasResponseEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESIsdbCasResponseEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc625c6f-84e8-4a82-b53c-717b33c10d04">GetDataLength</a>
</td>
<td align="left" width="63%">
Gets the length of the response data from the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3ab39b4-567f-49a5-b3d2-460ec648ab26">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the request identifier for the MSD that originated the CAS request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee0618a6-6162-4178-be44-978558add914">GetResponseData</a>
</td>
<td align="left" width="63%">
Gets the response data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status code from the response.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESIsdbCasResponseEvent)</code>.



