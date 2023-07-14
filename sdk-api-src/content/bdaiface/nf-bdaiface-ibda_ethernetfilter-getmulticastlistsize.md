---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastListSize
title: IBDA_EthernetFilter::GetMulticastListSize (bdaiface.h)
description: The GetMulticastListSize method retrieves the number of addresses currently in the list.
helpviewer_keywords: ["GetMulticastListSize","GetMulticastListSize method [Microsoft TV Technologies]","GetMulticastListSize method [Microsoft TV Technologies]","IBDA_EthernetFilter interface","IBDA_EthernetFilter interface [Microsoft TV Technologies]","GetMulticastListSize method","IBDA_EthernetFilter.GetMulticastListSize","IBDA_EthernetFilter::GetMulticastListSize","IBDA_EthernetFilterGetMulticastListSize","bdaiface/IBDA_EthernetFilter::GetMulticastListSize","mstv.ibda_ethernetfilter_getmulticastlistsize"]
old-location: mstv\ibda_ethernetfilter_getmulticastlistsize.htm
tech.root: mstv
ms.assetid: bc2452ca-53ad-4286-951a-c211f3f82cf3
ms.date: 12/05/2018
ms.keywords: GetMulticastListSize, GetMulticastListSize method [Microsoft TV Technologies], GetMulticastListSize method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastListSize method, IBDA_EthernetFilter.GetMulticastListSize, IBDA_EthernetFilter::GetMulticastListSize, IBDA_EthernetFilterGetMulticastListSize, bdaiface/IBDA_EthernetFilter::GetMulticastListSize, mstv.ibda_ethernetfilter_getmulticastlistsize
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
 - IBDA_EthernetFilter::GetMulticastListSize
 - bdaiface/IBDA_EthernetFilter::GetMulticastListSize
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
 - IBDA_EthernetFilter.GetMulticastListSize
---

# IBDA_EthernetFilter::GetMulticastListSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMulticastListSize</b> method retrieves the number of addresses currently in the list.

## -parameters

### -param pulcbAddresses [out]

Pointer that receives the number of addresses currently in the Network Provider's list.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Addresses in the address list are byte aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an Ethernet address.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ethernetfilter">IBDA_EthernetFilter Interface</a>