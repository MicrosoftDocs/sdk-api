---
UID: NN:bdaiface.IBDA_IPV6Filter
title: IBDA_IPV6Filter (bdaiface.h)
description: This interface is not supported.
helpviewer_keywords: ["IBDA_IPV6Filter","IBDA_IPV6Filter interface [Microsoft TV Technologies]","IBDA_IPV6Filter interface [Microsoft TV Technologies]","described","IBDA_IPV6FilterInterface","bdaiface/IBDA_IPV6Filter","mstv.ibda_ipv6filter"]
old-location: mstv\ibda_ipv6filter.htm
tech.root: mstv
ms.assetid: b506d382-c56d-4c5b-ad57-e186173ea9a8
ms.date: 12/05/2018
ms.keywords: IBDA_IPV6Filter, IBDA_IPV6Filter interface [Microsoft TV Technologies], IBDA_IPV6Filter interface [Microsoft TV Technologies],described, IBDA_IPV6FilterInterface, bdaiface/IBDA_IPV6Filter, mstv.ibda_ipv6filter
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
 - IBDA_IPV6Filter
 - bdaiface/IBDA_IPV6Filter
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
 - IBDA_IPV6Filter
---

# IBDA_IPV6Filter interface


## -description

This interface is not supported.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_IPV6Filter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_IPV6Filter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_IPV6Filter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv6filter-getmulticastlist">GetMulticastList</a>
</td>
<td align="left" width="63%">
Retrieves the list of multicast addresses stored by the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv6filter-getmulticastlistsize">GetMulticastListSize</a>
</td>
<td align="left" width="63%">
Retrieves the size in bytes of the list of multicast addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv6filter-getmulticastmode">GetMulticastMode</a>
</td>
<td align="left" width="63%">
Retrieves the mode(s) of the multicast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv6filter-putmulticastlist">PutMulticastList</a>
</td>
<td align="left" width="63%">
Specifies the parameters of the multicast list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv4filter-putmulticastmode">PutMulticastMode</a>
</td>
<td align="left" width="63%">
Specifies the mode(s) of the multicast.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPV6Filter)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>

