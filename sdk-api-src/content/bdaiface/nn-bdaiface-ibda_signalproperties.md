---
UID: NN:bdaiface.IBDA_SignalProperties
title: IBDA_SignalProperties
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibda_signalproperties.htm
tech.root: mstv
ms.assetid: fe88b628-7959-4d2f-981f-7de9126146f6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_SignalProperties, IBDA_SignalProperties interface [Microsoft TV Technologies], IBDA_SignalProperties interface [Microsoft TV Technologies],described, IBDA_SignalPropertiesInterface, bdaiface/IBDA_SignalProperties, mstv.ibda_signalproperties
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
 - Bdaiface.h
api_name:
 - IBDA_SignalProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_SignalProperties interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IBDA_SignalProperties</b> interface is implemented by a BDA device filter. Through this interface, the network provider informs a BDA device filter about the current tuning request. The network provider calls the <b>PutXxx</b> methods in the interface at the time that the BDA device is registered with the network provider. Thereafter, the network provider calls these methods whenever the current tuning request is modified.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_SignalProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_SignalProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_SignalProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c799cad-2371-4845-a783-e7227fb81c4c">GetNetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/929ec042-3f43-468e-944a-919dda3893be">GetSignalSource</a>
</td>
<td align="left" width="63%">
Retrieves the signal source for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03738363-5923-4e26-a0ea-e345b927140c">GetTuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the tuning space for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e92fa253-7e00-457f-805e-ed13bca84254">PutNetworkType</a>
</td>
<td align="left" width="63%">
Specifies the network type for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81cd43b1-97a7-4663-984e-2c20a8315c7e">PutSignalSource</a>
</td>
<td align="left" width="63%">
Specifies the signal source for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3ecddfc-a95b-47ba-8a2b-5073de4aad5e">PutTuningSpace</a>
</td>
<td align="left" width="63%">
Specifies the tuning space for the current tuning request.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_SignalProperties)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

