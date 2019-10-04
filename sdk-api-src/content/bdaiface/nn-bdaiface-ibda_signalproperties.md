---
UID: NN:bdaiface.IBDA_SignalProperties
title: IBDA_SignalProperties (bdaiface.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibda_signalproperties.htm
tech.root: mstv
ms.assetid: fe88b628-7959-4d2f-981f-7de9126146f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_SignalProperties, IBDA_SignalProperties interface [Microsoft TV Technologies], IBDA_SignalProperties interface [Microsoft TV Technologies],described, IBDA_SignalPropertiesInterface, bdaiface/IBDA_SignalProperties, mstv.ibda_signalproperties
ms.topic: interface
f1_keywords: 
 - "bdaiface/IBDA_SignalProperties"
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
 - Bdaiface.h
api_name:
 - IBDA_SignalProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_SignalProperties interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IBDA_SignalProperties</b> interface is implemented by a BDA device filter. Through this interface, the network provider informs a BDA device filter about the current tuning request. The network provider calls the <b>PutXxx</b> methods in the interface at the time that the BDA device is registered with the network provider. Thereafter, the network provider calls these methods whenever the current tuning request is modified.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_SignalProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_SignalProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-getnetworktype">GetNetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-getsignalsource">GetSignalSource</a>
</td>
<td align="left" width="63%">
Retrieves the signal source for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-gettuningspace">GetTuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the tuning space for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-putnetworktype">PutNetworkType</a>
</td>
<td align="left" width="63%">
Specifies the network type for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-putsignalsource">PutSignalSource</a>
</td>
<td align="left" width="63%">
Specifies the signal source for the current tuning request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalproperties-puttuningspace">PutTuningSpace</a>
</td>
<td align="left" width="63%">
Specifies the tuning space for the current tuning request.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_SignalProperties)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

