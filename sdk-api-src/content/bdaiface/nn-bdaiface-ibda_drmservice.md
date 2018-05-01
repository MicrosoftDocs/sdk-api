---
UID: NN:bdaiface.IBDA_DRMService
title: IBDA_DRMService
author: windows-driver-content
description: Provides access to a device's Digital Rights Management (DRM) Service.
old-location: mstv\ibda_drmservice.htm
old-project: mstv
ms.assetid: bd06118c-ea1b-46e4-b499-67039430a52e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBDA_DRMService, IBDA_DRMService interface [Microsoft TV Technologies], IBDA_DRMService interface [Microsoft TV Technologies], described, bdaiface/IBDA_DRMService, mstv.ibda_drmservice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	IBDA_DRMService
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_DRMService interface


## -description


Provides access to a device's Digital Rights Management (DRM) Service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DRMService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_DRMService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DRMService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/474ea991-6fb4-4eb4-9146-c76914765dc1">GetDRMStatus</a>
</td>
<td align="left" width="63%">
Gets the current DRM status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89da348f-c79c-4c77-8270-51a71b0a1a89">SetDRM</a>
</td>
<td align="left" width="63%">
Activates a DRM system on the media transform device (MTD).

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DRMService)</code>.



