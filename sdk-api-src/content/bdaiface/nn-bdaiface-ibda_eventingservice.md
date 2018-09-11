---
UID: NN:bdaiface.IBDA_EventingService
title: IBDA_EventingService
author: windows-sdk-content
description: Provides access to a device's Eventing Service.
old-location: mstv\ibda_eventingservice.htm
tech.root: mstv
ms.assetid: 45ef0b45-92d0-47c1-9334-d0df74a43d28
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_EventingService, IBDA_EventingService interface [Microsoft TV Technologies], IBDA_EventingService interface [Microsoft TV Technologies],described, bdaiface/IBDA_EventingService, mstv.ibda_eventingservice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_EventingService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_EventingService interface


## -description


Provides access to a device's Eventing Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_EventingService</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBDA_EventingService</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBDA_EventingService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693346(v=VS.85).aspx">CompleteEvent</a>
</td>
<td align="left" width="63%">
Notifies the media transform device (MTD) in a graph when a media sink device (MSD) completes an event.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_EventingService)</code>.



