---
UID: NN:bdaiface.IBDA_IPSinkControl
title: IBDA_IPSinkControl
author: windows-sdk-content
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.
old-location: mstv\ibda_ipsinkcontrol.htm
tech.root: mstv
ms.assetid: 3665c06e-0e9f-4a8a-bb72-eb0c402ce7c9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_IPSinkControl, IBDA_IPSinkControl interface [Microsoft TV Technologies], IBDA_IPSinkControl interface [Microsoft TV Technologies],described, IBDA_IPSinkControlInterface, bdaiface/IBDA_IPSinkControl, mstv.ibda_ipsinkcontrol
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
req.idl: 
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
 - IBDA_IPSinkControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_IPSinkControl interface


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        

The <b>IBDA_IPSinkControl</b> interface is implemented on the <a href="https://msdn.microsoft.com/en-us/library/Dd693009(v=VS.85).aspx">BDA IP Sink</a> filter, which manages the delivery of in-band IP data to the network stack. This interface is superseded by <a href="https://msdn.microsoft.com/en-us/library/Dd693378(v=VS.85).aspx">IBDA_IPSinkInfo</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPSinkControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBDA_IPSinkControl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693376(v=VS.85).aspx">GetAdapterIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the IP address of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693377(v=VS.85).aspx">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the multicast addresses to which the IP Sink filter is listening.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPSinkControl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693008(v=VS.85).aspx">BDA Interfaces</a>
 

 

