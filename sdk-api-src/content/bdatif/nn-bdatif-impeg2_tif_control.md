---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMPEG2_TIF_CONTROL interface


## -description


<p class="CCE_Message">[<b>IMPEG2_TIF_CONTROL</b> is no longer available for use. Instead, use the <a href="https://msdn.microsoft.com/96c76a81-57c9-4c4b-a5f6-7b9862757847">IBDA_TIF_REGISTRATION</a> interface to register the TIF with the Network Provider, and use the <a href="https://msdn.microsoft.com/45c09a02-7da8-460a-9a64-f012c2181b94">IMPEG2PIDMap</a> interface to map or unmap PIDs.]

The <b>IMPEG2_TIF_CONTROL</b> interface is implemented by the <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a>. A Transport Information Filter (TIF) can use this interface to register itself and request table sections carried on specific PIDs within the transport stream. The Network Provider Filter instructs the <a href="https://msdn.microsoft.com/99bfc55d-6519-4e85-98ce-cad27bd71ffb">MPEG-2 Demultiplexer</a> (Demux) to send or stop sending the specified packets to the TIF's input pin. All sections are delivered by the Demux to the TIF as complete MPEG-2 table sections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2_TIF_CONTROL</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMPEG2_TIF_CONTROL</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2_TIF_CONTROL</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27add7cc-1d77-4ac5-b63f-757f63f4c9b8">AddPIDs</a>
</td>
<td align="left" width="63%">

          Notifies the Network Provider which PIDs the TIF should receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5188e30-6980-482f-a690-494855d6aeea">DeletePIDs</a>
</td>
<td align="left" width="63%">
Informs the Network Provider that the TIF no longer requires the specified PID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d77c3d8-b91c-43de-b4c1-bd41636eb4ad">GetPIDCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of MPEG-2 Packet IDs being filtered by the Demux into the TIF's input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7ca141b-e471-47ce-96b5-b2c0cad89daf">GetPIDs</a>
</td>
<td align="left" width="63%">
Retrieves the list of MPEG-2 Packet IDs being filtered into the TIF's input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d17b1f6b-24f4-40f4-9a58-aa582c0958f8">RegisterTIF</a>
</td>
<td align="left" width="63%">
Called by the Transport Information Filter to register itself with the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4fd151e-ec24-41b9-85df-fba05fc174d1">UnregisterTIF</a>
</td>
<td align="left" width="63%">
Called by the Transport Information Filter to unregister itself with the Network Provider.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2_TIF_CONTROL)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

