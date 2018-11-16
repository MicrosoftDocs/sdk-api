---
UID: NN:bdaiface.ICCSubStreamFiltering
title: ICCSubStreamFiltering
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iccsubstreamfiltering.htm
tech.root: mstv
ms.assetid: 2de6796d-beb3-4611-a559-449fe21193a6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICCSubStreamFiltering, ICCSubStreamFiltering interface [Microsoft TV Technologies], ICCSubStreamFiltering interface [Microsoft TV Technologies],described, ICCSubStreamFilteringInterface, bdaiface/ICCSubStreamFiltering, mstv.iccsubstreamfiltering
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
        

The <b>ICCSubStreamFiltering</b> interface sets the filtering on the closed captioning (CC) pins of the <a href="https://msdn.microsoft.com/en-us/library/Dd695343(v=VS.85).aspx">VBICodec</a> filter. The CC output pins on the VBICodec filter both expose this interface. Use this interface to select which CC services are delivered by each pin. The CC pins are independent, so you can select different services on each pin. For example, you might select CC1 and CC2 on one pin and extended data services (XDS) on the other.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICCSubStreamFiltering</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICCSubStreamFiltering</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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




<a href="https://msdn.microsoft.com/en-us/library/Dd693008(v=VS.85).aspx">BDA Interfaces</a>
 

 

