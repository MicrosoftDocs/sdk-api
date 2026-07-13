---
UID: NF:bdaiface.IBDA_IPV6Filter.GetMulticastList
title: IBDA_IPV6Filter::GetMulticastList (bdaiface.h)
description: The GetMulticastList method retrieves the list of multicast addresses on the Network Provider.
helpviewer_keywords: ["GetMulticastList","GetMulticastList method [Microsoft TV Technologies]","GetMulticastList method [Microsoft TV Technologies]","IBDA_IPV6Filter interface","IBDA_IPV6Filter interface [Microsoft TV Technologies]","GetMulticastList method","IBDA_IPV6Filter.GetMulticastList","IBDA_IPV6Filter::GetMulticastList","IBDA_IPV6FilterGetMulticastList","bdaiface/IBDA_IPV6Filter::GetMulticastList","mstv.ibda_ipv6filter_getmulticastlist"]
old-location: mstv\ibda_ipv6filter_getmulticastlist.htm
tech.root: mstv
ms.assetid: 545c6bcb-f96c-47d7-ac33-92da016dbabf
ms.date: 12/05/2018
ms.keywords: GetMulticastList, GetMulticastList method [Microsoft TV Technologies], GetMulticastList method [Microsoft TV Technologies],IBDA_IPV6Filter interface, IBDA_IPV6Filter interface [Microsoft TV Technologies],GetMulticastList method, IBDA_IPV6Filter.GetMulticastList, IBDA_IPV6Filter::GetMulticastList, IBDA_IPV6FilterGetMulticastList, bdaiface/IBDA_IPV6Filter::GetMulticastList, mstv.ibda_ipv6filter_getmulticastlist
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
 - IBDA_IPV6Filter::GetMulticastList
 - bdaiface/IBDA_IPV6Filter::GetMulticastList
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
 - IBDA_IPV6Filter.GetMulticastList
---

# IBDA_IPV6Filter::GetMulticastList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMulticastList</b> method retrieves the list of multicast addresses on the Network Provider.

## -parameters

### -param pulcbAddresses [in, out]

On input, specifies the maximum number of addresses to retrieve, multiplied by the number of bytes per address. On output, receives the actual number of bytes retrieved.

### -param pAddressList [out]

Pointer that receives an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The declaration of <i>pAddressList</i> is not COM compliant. As a workaround, the client should allocate the <i>pAddressList</i> buffer. The buffer should be the same size as advertised in the <i>pulcbAddresses</i> parameter. The network provider will just fill in the buffer allocated by the caller.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv4filter">IBDA_IPV4Filter Interface</a>