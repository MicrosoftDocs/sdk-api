---
UID: NN:bdaiface.IBDA_IPV4Filter
title: IBDA_IPV4Filter
author: windows-sdk-content
description: The IBDA_ IPV4Filter interface is implemented on a Network Provider.
old-location: mstv\ibda_ipv4filter.htm
old-project: mstv
ms.assetid: 3db86e21-6d05-4b7f-be83-a3fa506a0e3b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_IPV4Filter, IBDA_IPV4Filter interface [Microsoft TV Technologies], IBDA_IPV4Filter interface [Microsoft TV Technologies],described, IBDA_IPV4FilterInterface, bdaiface/IBDA_IPV4Filter, mstv.ibda_ipv4filter
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
 - IBDA_IPV4Filter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_IPV4Filter interface


## -description



The <b>IBDA_ IPV4Filter</b> interface is implemented on a Network Provider. The methods are called by the BDA IPSink filter in order to give the Network Provider a list of multicast Ethernet addresses being requested by an application. The Network Provider then informs all registered transport information filters (TIFs) of the new addresses. The TIF(s) are responsible for mapping those addresses to PIDs and passing the PIDs back to the Network Provider, which then resets the PID list for the IP data output pin on the MPEG-2 Demultiplexer. This causes the IP data on the specified PIDs to be routed through the data services segment of the graph and on to Winsock where the listening application can receive it. The <a href="https://msdn.microsoft.com/f4f9d6c0-0acf-416b-adb3-643ac0167d0a">IBDA_EthernetFilter</a> interface performs the same function for Ethernet multicast addresses.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPV4Filter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_IPV4Filter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_IPV4Filter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/020a4053-76ba-4e67-afa8-27abcf70c456">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves the list of multicast addresses stored by the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d31e34f-1997-40fe-9b32-a193d3017798">GetMulticastListSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of addresses in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/231c20f6-3204-48a3-ad07-3df9c6d87bd7">GetMulticastMode</a>
</td>
<td align="left" width="63%">
Retrieves the multicast mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06b93c7d-662e-408b-94e3-137287160898">PutMulticastList</a>
</td>
<td align="left" width="63%">
Specifies the list of multicast addresses on the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0a12c21-e196-4228-9994-51047271cf57">PutMulticastMode</a>
</td>
<td align="left" width="63%">
Specifies the multicast mode.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_ IPV4Filter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

