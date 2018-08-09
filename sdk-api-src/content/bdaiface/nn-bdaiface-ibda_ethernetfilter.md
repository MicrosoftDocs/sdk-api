---
UID: NN:bdaiface.IBDA_EthernetFilter
title: IBDA_EthernetFilter
author: windows-sdk-content
description: The IBDA_EthernetFilter interface is implemented on a Network Provider.
old-location: mstv\ibda_ethernetfilter.htm
old-project: mstv
ms.assetid: f4f9d6c0-0acf-416b-adb3-643ac0167d0a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_EthernetFilter, IBDA_EthernetFilter interface [Microsoft TV Technologies], IBDA_EthernetFilter interface [Microsoft TV Technologies],described, IBDA_EthernetFilterInterface, bdaiface/IBDA_EthernetFilter, mstv.ibda_ethernetfilter
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
 - IBDA_EthernetFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_EthernetFilter interface


## -description



The <b>IBDA_EthernetFilter</b> interface is implemented on a Network Provider. The methods are called by the BDA IPSink filter in order to give the Network Provider a list of multicast Ethernet addresses being requested by an application. The Network Provider then informs all registered transport information filters (TIFs) of the new addresses. The TIF(s) are responsible for mapping those addresses to PIDs and passing the PIDs back to the Network Provider, which then resets the PID list for the IP data output pin on the MPEG-2 Demultiplexer. This causes the IP data on the specified PIDs to be routed through the data services segment of the graph and on to Winsock where the listening application can receive it. The <a href="https://msdn.microsoft.com/3db86e21-6d05-4b7f-be83-a3fa506a0e3b">IBDA_IPV4Filter</a> interface performs the same function for IPv4 multicast addresses.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_EthernetFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_EthernetFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_EthernetFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65ad05c7-eb0e-450e-9bec-d46738f65dcd">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves the list of multicast addresses stored by the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc2452ca-53ad-4286-951a-c211f3f82cf3">GetMulticastListSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of addresses currently in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a0a5dbb-642a-458b-a5b2-80e993ab61ca">GetMulticastMode</a>
</td>
<td align="left" width="63%">
Retrieves the multicast mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0398dc58-07be-40cd-95af-62b29a191d3c">PutMulticastList</a>
</td>
<td align="left" width="63%">
Specifies the list of multicast addresses on the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01694aba-6b43-46da-a35c-7f3f5befecad">PutMulticastMode</a>
</td>
<td align="left" width="63%">
Specifies the multicast mode.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_EthernetFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

