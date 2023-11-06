---
UID: NF:bdaiface.IBDA_IPV4Filter.PutMulticastList
title: IBDA_IPV4Filter::PutMulticastList (bdaiface.h)
description: The PutMulticastList method sets the list of multicast addresses on the Network Provider.
helpviewer_keywords: ["IBDA_IPV4Filter interface [Microsoft TV Technologies]","PutMulticastList method","IBDA_IPV4Filter.PutMulticastList","IBDA_IPV4Filter::PutMulticastList","IBDA_IPV4FilterPutMulticastList","PutMulticastList","PutMulticastList method [Microsoft TV Technologies]","PutMulticastList method [Microsoft TV Technologies]","IBDA_IPV4Filter interface","bdaiface/IBDA_IPV4Filter::PutMulticastList","mstv.ibda_ipv4filter_putmulticastlist"]
old-location: mstv\ibda_ipv4filter_putmulticastlist.htm
tech.root: mstv
ms.assetid: 06b93c7d-662e-408b-94e3-137287160898
ms.date: 12/05/2018
ms.keywords: IBDA_IPV4Filter interface [Microsoft TV Technologies],PutMulticastList method, IBDA_IPV4Filter.PutMulticastList, IBDA_IPV4Filter::PutMulticastList, IBDA_IPV4FilterPutMulticastList, PutMulticastList, PutMulticastList method [Microsoft TV Technologies], PutMulticastList method [Microsoft TV Technologies],IBDA_IPV4Filter interface, bdaiface/IBDA_IPV4Filter::PutMulticastList, mstv.ibda_ipv4filter_putmulticastlist
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
 - IBDA_IPV4Filter::PutMulticastList
 - bdaiface/IBDA_IPV4Filter::PutMulticastList
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
 - IBDA_IPV4Filter.PutMulticastList
---

# IBDA_IPV4Filter::PutMulticastList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>PutMulticastList</b> method sets the list of multicast addresses on the Network Provider.

## -parameters

### -param ulcbAddresses [in]

Specifies the number of addresses in the list, times the number of bytes per address.

### -param pAddressList [in]

Pointer that receives an array of addresses whose size in bytes is equal to <i>ulcbAddresses</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv4filter">IBDA_IPV4Filter Interface</a>