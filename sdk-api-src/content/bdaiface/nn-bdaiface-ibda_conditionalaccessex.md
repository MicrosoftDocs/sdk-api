---
UID: NN:bdaiface.IBDA_ConditionalAccessEx
title: IBDA_ConditionalAccessEx
author: windows-driver-content
description: Provides access to a device's Conditional Access Service (CAS), which manages access to protected content.
old-location: mstv\ibda_conditionalaccessex.htm
old-project: mstv
ms.assetid: 9db9b6b1-fc4f-48f0-940e-d79a321ef094
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBDA_ConditionalAccessEx, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies], IBDA_ConditionalAccessEx interface [Microsoft TV Technologies], described, bdaiface/IBDA_ConditionalAccessEx, mstv.ibda_conditionalaccessex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_ConditionalAccessEx
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_ConditionalAccessEx interface


## -description


Provides access to a device's Conditional Access Service (CAS), which manages access to protected content. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_ConditionalAccessEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_ConditionalAccessEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_ConditionalAccessEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea581065-b10b-4a2a-9090-99d6fd140ea9">CheckEntitlementToken</a>
</td>
<td align="left" width="63%">
Checks the access availability of content that is identified by an entitlement token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30cba76b-ae52-4c87-a88e-faa9ad3f12f9">CloseMmiDialog</a>
</td>
<td align="left" width="63%">
Notifies the CAS that the media sink device (MSD) has closed a user interface (MMI) dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cabe06c8-ead5-4e1d-83c3-e7b96b05fc4a">CreateDialogRequestNumber</a>
</td>
<td align="left" width="63%">
Gets a new dialog request number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15390805-ff09-4dca-b00d-ad2f3641911b">OpenBroadcastMmi</a>
</td>
<td align="left" width="63%">
Responds to a BroadcastMMI event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9e3d319-c76c-45df-aca3-d5447605b7c0">SetCaptureToken</a>
</td>
<td align="left" width="63%">
Requests special events that are identified by a capture token.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_ConditionalAccessEx)</code>.



