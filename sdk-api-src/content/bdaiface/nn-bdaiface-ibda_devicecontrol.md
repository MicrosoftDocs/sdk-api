---
UID: NN:bdaiface.IBDA_DeviceControl
title: IBDA_DeviceControl (bdaiface.h)
description: The IBDA_DeviceControl interface is implemented on all BDA device filters.
helpviewer_keywords: ["IBDA_DeviceControl","IBDA_DeviceControl interface [Microsoft TV Technologies]","IBDA_DeviceControl interface [Microsoft TV Technologies]","described","IBDA_DeviceControlInterface","bdaiface/IBDA_DeviceControl","mstv.ibda_devicecontrol"]
old-location: mstv\ibda_devicecontrol.htm
tech.root: mstv
ms.assetid: 41e167b0-100e-41d2-8759-0411a10931ae
ms.date: 12/05/2018
ms.keywords: IBDA_DeviceControl, IBDA_DeviceControl interface [Microsoft TV Technologies], IBDA_DeviceControl interface [Microsoft TV Technologies],described, IBDA_DeviceControlInterface, bdaiface/IBDA_DeviceControl, mstv.ibda_devicecontrol
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_DeviceControl
 - bdaiface/IBDA_DeviceControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DeviceControl
---

# IBDA_DeviceControl interface


## -description

The <b>IBDA_DeviceControl</b> interface is implemented on all BDA device filters. 

The methods provided by this interface are called by a Network Provider to control a BDA device. Each instance of a device has one transaction list. A Network Provider first calls the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-startchanges">StartChanges</a> method. This deletes any previous uncommitted changes that were still pending. Then a Network Provider modifies whatever properties on the filter are required for the particular tuning operation. Then it calls the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-checkchanges">CheckChanges</a> method to determine whether the modifications will be successful, without instructing the filter to actually make the changes. If this call succeeds, then a Network Provider calls <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-commitchanges">CommitChanges</a> to cause the filter to actually modify the specified properties. For more information, see "Changing BDA Filter Properties" in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DeviceControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_DeviceControl</b> also has these types of members:
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
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-checkchanges">CheckChanges</a>
</td>
<td align="left" width="63%">
Queries the device filter as to whether the changes that are pending would succeed if they were committed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-commitchanges">CommitChanges</a>
</td>
<td align="left" width="63%">
Instructs the device to perform the changes specified in the previous call to <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-startchanges">StartChanges</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-getchangestate">GetChangeState</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether any uncommitted changes are currently pending in the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_devicecontrol-startchanges">StartChanges</a>
</td>
<td align="left" width="63%">
Called by a Network Provider before it begins to modify a set of properties on a BDA device filter.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DeviceControl)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>