---
UID: NN:bdaiface.IBDA_NetworkProvider
title: IBDA_NetworkProvider (bdaiface.h)
author: windows-sdk-content
description: The IBDA_NetworkProvider interface is implemented on a Network Provider filter. It provides methods that BDA device filters call to register themselves after they are added to the graph.
old-location: mstv\ibda_networkprovider.htm
tech.root: mstv
ms.assetid: 84b6cd51-4cb5-4a43-9ac2-88ca8049b950
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_NetworkProvider, IBDA_NetworkProvider interface [Microsoft TV Technologies], IBDA_NetworkProvider interface [Microsoft TV Technologies],described, IBDA_NetworkProviderInterface, bdaiface/IBDA_NetworkProvider, mstv.ibda_networkprovider
ms.topic: interface
f1_keywords: 
 - "bdaiface/IBDA_NetworkProvider"
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
 - IBDA_NetworkProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_NetworkProvider interface


## -description



The <b>IBDA_NetworkProvider</b> interface is implemented on a Network Provider filter. It provides methods that BDA device filters call to register themselves after they are added to the graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_NetworkProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_NetworkProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_NetworkProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-getnetworktype">GetNetworkType</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-getsignalsource">GetSignalSource</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-gettuningspace">GetTuningSpace</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to retrieve the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-putsignalsource">PutSignalSource</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to specify the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-puttuningspace">PutTuningSpace</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to specify the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-registerdevicefilter">RegisterDeviceFilter</a>
</td>
<td align="left" width="63%">
Called by a BDA device filter to register itself in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-unregisterdevicefilter">UnRegisterDeviceFilter</a>
</td>
<td align="left" width="63%">
Called by BDA device filters when they are removed from the filter graph.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NetworkProvider)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

