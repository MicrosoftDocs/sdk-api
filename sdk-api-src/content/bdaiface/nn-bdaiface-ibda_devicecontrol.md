---
UID: NN:bdaiface.IBDA_DeviceControl
title: IBDA_DeviceControl
author: windows-driver-content
description: The IBDA_DeviceControl interface is implemented on all BDA device filters.
old-location: mstv\ibda_devicecontrol.htm
old-project: mstv
ms.assetid: 41e167b0-100e-41d2-8759-0411a10931ae
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IBDA_DeviceControl, IBDA_DeviceControl interface [Microsoft TV Technologies], IBDA_DeviceControl interface [Microsoft TV Technologies],described, IBDA_DeviceControlInterface, bdaiface/IBDA_DeviceControl, mstv.ibda_devicecontrol
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_DeviceControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_DeviceControl interface


## -description


The <b>IBDA_DeviceControl</b> interface is implemented on all BDA device filters. 

The methods provided by this interface are called by a Network Provider to control a BDA device. Each instance of a device has one transaction list. A Network Provider first calls the <a href="https://msdn.microsoft.com/989cdd9b-ea5b-4a80-b157-9469a210b966">StartChanges</a> method. This deletes any previous uncommitted changes that were still pending. Then a Network Provider modifies whatever properties on the filter are required for the particular tuning operation. Then it calls the <a href="https://msdn.microsoft.com/e4654041-d17b-4b1b-9d0f-23c00b0090ea">CheckChanges</a> method to determine whether the modifications will be successful, without instructing the filter to actually make the changes. If this call succeeds, then a Network Provider calls <a href="https://msdn.microsoft.com/1f55346b-1d32-4eb9-84ef-4671cdd2bc61">CommitChanges</a> to cause the filter to actually modify the specified properties. For more information, see "Changing BDA Filter Properties" in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DeviceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_DeviceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DeviceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4654041-d17b-4b1b-9d0f-23c00b0090ea">CheckChanges</a>
</td>
<td align="left" width="63%">
Queries the device filter as to whether the changes that are pending would succeed if they were committed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f55346b-1d32-4eb9-84ef-4671cdd2bc61">CommitChanges</a>
</td>
<td align="left" width="63%">
Instructs the device to perform the changes specified in the previous call to <a href="https://msdn.microsoft.com/989cdd9b-ea5b-4a80-b157-9469a210b966">StartChanges</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a36763-552a-44dc-8068-90f1b8fe09e5">GetChangeState</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether any uncommitted changes are currently pending in the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/989cdd9b-ea5b-4a80-b157-9469a210b966">StartChanges</a>
</td>
<td align="left" width="63%">
Called by a Network Provider before it begins to modify a set of properties on a BDA device filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DeviceControl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

