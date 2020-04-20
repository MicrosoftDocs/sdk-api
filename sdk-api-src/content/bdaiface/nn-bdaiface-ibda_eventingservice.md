---
UID: NN:bdaiface.IBDA_EventingService
title: IBDA_EventingService (bdaiface.h)
description: Provides access to a device's Eventing Service.helpviewer_keywords: ["IBDA_EventingService","IBDA_EventingService interface [Microsoft TV Technologies]","IBDA_EventingService interface [Microsoft TV Technologies]","described","bdaiface/IBDA_EventingService","mstv.ibda_eventingservice"]
old-location: mstv\ibda_eventingservice.htm
tech.root: mstv
ms.assetid: 45ef0b45-92d0-47c1-9334-d0df74a43d28
ms.date: 12/05/2018
ms.keywords: IBDA_EventingService, IBDA_EventingService interface [Microsoft TV Technologies], IBDA_EventingService interface [Microsoft TV Technologies],described, bdaiface/IBDA_EventingService, mstv.ibda_eventingservice
f1_keywords:
- bdaiface/IBDA_EventingService
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_EventingService interface


## -description


Provides access to a device's Eventing Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_EventingService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_EventingService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_eventingservice-completeevent">CompleteEvent</a>
</td>
<td align="left" width="63%">
Notifies the media transform device (MTD) in a graph when a media sink device (MSD) completes an event.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_EventingService)</code>.



