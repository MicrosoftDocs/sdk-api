---
UID: NN:bdaiface.IBDA_PinControl
title: IBDA_PinControl (bdaiface.h)
author: windows-sdk-content
description: The IBDA_PinControl interface is exposed on a BDA device filter's pins. A Network Provider calls these methods to determine the type and identifier of each pin on the filter. A Network Provider uses this information when building the graph.
old-location: mstv\ibda_pincontrol.htm
tech.root: mstv
ms.assetid: 2d318cc4-b3f2-4fb6-b9e3-8ba8312ad2ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_PinControl, IBDA_PinControl interface [Microsoft TV Technologies], IBDA_PinControl interface [Microsoft TV Technologies],described, IBDA_PinControlInterface, bdaiface/IBDA_PinControl, mstv.ibda_pincontrol
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
 - IBDA_PinControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_PinControl interface


## -description



The <b>IBDA_PinControl</b> interface is exposed on a BDA device filter's pins. A Network Provider calls these methods to determine the type and identifier of each pin on the filter. A Network Provider uses this information when building the graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_PinControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_PinControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_PinControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693422(v=VS.85).aspx">GetPinID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693423(v=VS.85).aspx">GetPinType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693424(v=VS.85).aspx">RegistrationContext</a>
</td>
<td align="left" width="63%">
Retrieves the registration context of a particular pin.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_PinControl)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

