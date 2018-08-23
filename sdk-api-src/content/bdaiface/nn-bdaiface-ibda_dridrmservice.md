---
UID: NN:bdaiface.IBDA_DRIDRMService
title: IBDA_DRIDRMService
author: windows-sdk-content
description: The IBDA_DRIDRMService interface implements a Digital Rights Management (DRM) service for Media Transform Devices (MTDs) under the Protected Broadcast Driver Architecture (PBDA).
old-location: mstv\ibda_dridrmservice.htm
old-project: mstv
ms.assetid: 9b04c960-a766-4322-bf18-e59176ee2ad1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_DRIDRMService, IBDA_DRIDRMService interface [DirectShow], IBDA_DRIDRMService interface [DirectShow],described, bdaiface/IBDA_DRIDRMService, mstv.ibda_dridrmservice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DRIDRMService
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_DRIDRMService interface


## -description


The <b>IBDA_DRIDRMService</b> interface implements a Digital Rights Management (DRM) service for Media Transform Devices (MTDs) under the Protected Broadcast Driver Architecture (PBDA). This service allows conditional-access (CA) content to move between an MTD and a Media Sink Device (MSD) under DRM protection in a PBDA graph.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DRIDRMService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_DRIDRMService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DRIDRMService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/145e4716-05e1-41b8-98f3-72e719ca8b9f">GetDRMStatus</a>
</td>
<td align="left" width="63%">
Gets status information about the supported DRM services  that are set for an MTD. 
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01918e99-17e6-4c24-bb85-ba71cf68cf09">GetPairingStatus</a>
</td>
<td align="left" width="63%">
Gets status information about secure pairing between an MTD and an MSD in the graph.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95e59f33-0ff4-4618-b1e8-c43fe60b9434">SetDRM</a>
</td>
<td align="left" width="63%">
Sets the DRM service used by an MTD.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DRIDRMService)</code>.



