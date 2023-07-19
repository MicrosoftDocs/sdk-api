---
UID: NF:bdaiface.IBDA_IPV4Filter.GetMulticastListSize
title: IBDA_IPV4Filter::GetMulticastListSize (bdaiface.h)
description: The GetMulticastListSize method retrieves the number of addresses in the list.
helpviewer_keywords: ["GetMulticastListSize","GetMulticastListSize method [Microsoft TV Technologies]","GetMulticastListSize method [Microsoft TV Technologies]","IBDA_IPV4Filter interface","IBDA_IPV4Filter interface [Microsoft TV Technologies]","GetMulticastListSize method","IBDA_IPV4Filter.GetMulticastListSize","IBDA_IPV4Filter::GetMulticastListSize","IBDA_IPV4FilterGetMulticastListSize","bdaiface/IBDA_IPV4Filter::GetMulticastListSize","mstv.ibda_ipv4filter_getmulticastlistsize"]
old-location: mstv\ibda_ipv4filter_getmulticastlistsize.htm
tech.root: mstv
ms.assetid: 7d31e34f-1997-40fe-9b32-a193d3017798
ms.date: 12/05/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_IPV4Filter interface, IBDA_IPV4Filter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_IPV4Filter.GetMulticastListSize, IBDA_IPV4Filter::GetMulticastListSize, IBDA_IPV4FilterGetMulticastListSize, bdaiface/IBDA_IPV4Filter::GetMulticastListSize, mstv.ibda_ipv4filter_getmulticastlistsize
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
 - IBDA_IPV4Filter::GetMulticastListSize
 - bdaiface/IBDA_IPV4Filter::GetMulticastListSize
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
 - IBDA_IPV4Filter.GetMulticastListSize
---

# IBDA_IPV4Filter::GetMulticastListSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMulticastListSize</b> method retrieves the number of addresses in the list.

## -parameters

### -param pulcbAddresses [in, out]

Pointer that receives the number of addresses multiplied by the size of an IPv4 address.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is used by an IPv4 Network Data Sink filter to request that a Network Provider make its best effort to tune to the stream(s) on which a list of IPv4 multicast addresses may be transmitted. Addresses in the address list are byte-aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an IPv4 address.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv4filter">IBDA_IPV4Filter Interface</a>