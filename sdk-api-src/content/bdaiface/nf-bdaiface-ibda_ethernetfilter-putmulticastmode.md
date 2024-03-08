---
UID: NF:bdaiface.IBDA_EthernetFilter.PutMulticastMode
title: IBDA_EthernetFilter::PutMulticastMode (bdaiface.h)
description: The PutMulticastMode method sets the multicast mode.
helpviewer_keywords: ["IBDA_EthernetFilter interface [Microsoft TV Technologies]","PutMulticastMode method","IBDA_EthernetFilter.PutMulticastMode","IBDA_EthernetFilter::PutMulticastMode","IBDA_EthernetFilterPutMulticastMode","PutMulticastMode","PutMulticastMode method [Microsoft TV Technologies]","PutMulticastMode method [Microsoft TV Technologies]","IBDA_EthernetFilter interface","bdaiface/IBDA_EthernetFilter::PutMulticastMode","mstv.ibda_ethernetfilter_putmulticastmode"]
old-location: mstv\ibda_ethernetfilter_putmulticastmode.htm
tech.root: mstv
ms.assetid: 01694aba-6b43-46da-a35c-7f3f5befecad
ms.date: 12/05/2018
ms.keywords: IBDA_EthernetFilter interface [Microsoft TV Technologies],PutMulticastMode method, IBDA_EthernetFilter.PutMulticastMode, IBDA_EthernetFilter::PutMulticastMode, IBDA_EthernetFilterPutMulticastMode, PutMulticastMode, PutMulticastMode method [Microsoft TV Technologies], PutMulticastMode method [Microsoft TV Technologies],IBDA_EthernetFilter interface, bdaiface/IBDA_EthernetFilter::PutMulticastMode, mstv.ibda_ethernetfilter_putmulticastmode
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
 - IBDA_EthernetFilter::PutMulticastMode
 - bdaiface/IBDA_EthernetFilter::PutMulticastMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_EthernetFilter.PutMulticastMode
---

# IBDA_EthernetFilter::PutMulticastMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>PutMulticastMode</b> method sets the multicast mode.

## -parameters

### -param ulModeMask [in]

Specifies the multicast mode.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

See the Windows DDK for possible values.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ethernetfilter-getmulticastmode">GetMulticastMode</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ethernetfilter">IBDA_EthernetFilter Interface</a>