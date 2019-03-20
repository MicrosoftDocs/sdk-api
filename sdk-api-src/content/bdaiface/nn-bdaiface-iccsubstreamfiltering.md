---
UID: NN:bdaiface.ICCSubStreamFiltering
title: ICCSubStreamFiltering (bdaiface.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iccsubstreamfiltering.htm
tech.root: mstv
ms.assetid: 2de6796d-beb3-4611-a559-449fe21193a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICCSubStreamFiltering, ICCSubStreamFiltering interface [Microsoft TV Technologies], ICCSubStreamFiltering interface [Microsoft TV Technologies],described, ICCSubStreamFilteringInterface, bdaiface/ICCSubStreamFiltering, mstv.iccsubstreamfiltering
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
 - ICCSubStreamFiltering
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICCSubStreamFiltering interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>ICCSubStreamFiltering</b> interface sets the filtering on the closed captioning (CC) pins of the <a href="https://msdn.microsoft.com/51d43d2e-62fd-4366-a01f-5e6b37fc55fb">VBICodec</a> filter. The CC output pins on the VBICodec filter both expose this interface. Use this interface to select which CC services are delivered by each pin. The CC pins are independent, so you can select different services on each pin. For example, you might select CC1 and CC2 on one pin and extended data services (XDS) on the other.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICCSubStreamFiltering</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICCSubStreamFiltering</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICCSubStreamFiltering</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693502(v=VS.85).aspx">get_SubstreamTypes</a>
</td>
<td align="left" width="63%">
Retrieves the list of closed captioning services this pin is delivering

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693503(v=VS.85).aspx">put_SubstreamTypes</a>
</td>
<td align="left" width="63%">
Sets the closed captioning services the pin will deliver.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ICCSubStreamFiltering)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

