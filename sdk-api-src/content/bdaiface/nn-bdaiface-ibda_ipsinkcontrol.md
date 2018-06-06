---
UID: NN:bdaiface.IBDA_IPSinkControl
title: IBDA_IPSinkControl
author: windows-sdk-content
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.
old-location: mstv\ibda_ipsinkcontrol.htm
old-project: mstv
ms.assetid: 3665c06e-0e9f-4a8a-bb72-eb0c402ce7c9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_IPSinkControl, IBDA_IPSinkControl interface [Microsoft TV Technologies], IBDA_IPSinkControl interface [Microsoft TV Technologies],described, IBDA_IPSinkControlInterface, bdaiface/IBDA_IPSinkControl, mstv.ibda_ipsinkcontrol
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: 
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
 - IBDA_IPSinkControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_IPSinkControl interface


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        

The <b>IBDA_IPSinkControl</b> interface is implemented on the <a href="https://msdn.microsoft.com/78cd6cba-3bd7-4ad4-b65d-c6b866a18d4e">BDA IP Sink</a> filter, which manages the delivery of in-band IP data to the network stack. This interface is superseded by <a href="https://msdn.microsoft.com/fbbe12ea-964a-4a83-ac0a-ac8808bd9a63">IBDA_IPSinkInfo</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPSinkControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_IPSinkControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_IPSinkControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce9710e6-f611-4457-a282-9a7677b3055e">GetAdapterIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the IP address of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005cce5c-e8fb-49f0-8a75-b05cdd1f5e1b">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the multicast addresses to which the IP Sink filter is listening.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPSinkControl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

