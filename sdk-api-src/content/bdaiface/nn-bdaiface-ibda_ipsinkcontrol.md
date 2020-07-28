---
UID: NN:bdaiface.IBDA_IPSinkControl
title: IBDA_IPSinkControl (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.
helpviewer_keywords: ["IBDA_IPSinkControl","IBDA_IPSinkControl interface [Microsoft TV Technologies]","IBDA_IPSinkControl interface [Microsoft TV Technologies]","described","IBDA_IPSinkControlInterface","bdaiface/IBDA_IPSinkControl","mstv.ibda_ipsinkcontrol"]
old-location: mstv\ibda_ipsinkcontrol.htm
tech.root: mstv
ms.assetid: 3665c06e-0e9f-4a8a-bb72-eb0c402ce7c9
ms.date: 12/05/2018
ms.keywords: IBDA_IPSinkControl, IBDA_IPSinkControl interface [Microsoft TV Technologies], IBDA_IPSinkControl interface [Microsoft TV Technologies],described, IBDA_IPSinkControlInterface, bdaiface/IBDA_IPSinkControl, mstv.ibda_ipsinkcontrol
f1_keywords:
- bdaiface/IBDA_IPSinkControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_IPSinkControl interface


## -description



This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        

The <b>IBDA_IPSinkControl</b> interface is implemented on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-ip-sink-filter">BDA IP Sink</a> filter, which manages the delivery of in-band IP data to the network stack. This interface is superseded by <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkinfo">IBDA_IPSinkInfo</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPSinkControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_IPSinkControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipsinkcontrol-getadapteripaddress">GetAdapterIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the IP address of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipsinkcontrol-getmulticastlist">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the multicast addresses to which the IP Sink filter is listening.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPSinkControl)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

