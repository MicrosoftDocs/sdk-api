---
UID: NN:bdaiface.IBDA_ConditionalAccessEx
title: IBDA_ConditionalAccessEx
author: windows-sdk-content
description: Provides access to a device's Conditional Access Service (CAS), which manages access to protected content.
old-location: mstv\ibda_conditionalaccessex.htm
tech.root: mstv
ms.assetid: 9db9b6b1-fc4f-48f0-940e-d79a321ef094
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_ConditionalAccessEx, IBDA_ConditionalAccessEx interface [Microsoft TV Technologies], IBDA_ConditionalAccessEx interface [Microsoft TV Technologies],described, bdaiface/IBDA_ConditionalAccessEx, mstv.ibda_conditionalaccessex
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
 - IBDA_ConditionalAccessEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693263(v=VS.85).aspx">CheckEntitlementToken</a>
</td>
<td align="left" width="63%">
Checks the access availability of content that is identified by an entitlement token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693264(v=VS.85).aspx">CloseMmiDialog</a>
</td>
<td align="left" width="63%">
Notifies the CAS that the media sink device (MSD) has closed a user interface (MMI) dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693265(v=VS.85).aspx">CreateDialogRequestNumber</a>
</td>
<td align="left" width="63%">
Gets a new dialog request number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693266(v=VS.85).aspx">OpenBroadcastMmi</a>
</td>
<td align="left" width="63%">
Responds to a BroadcastMMI event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693267(v=VS.85).aspx">SetCaptureToken</a>
</td>
<td align="left" width="63%">
Requests special events that are identified by a capture token.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_ConditionalAccessEx)</code>.



