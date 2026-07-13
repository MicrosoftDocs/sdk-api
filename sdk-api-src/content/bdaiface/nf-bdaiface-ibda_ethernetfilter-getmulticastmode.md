---
UID: NF:bdaiface.IBDA_EthernetFilter.GetMulticastMode
title: IBDA_EthernetFilter::GetMulticastMode (bdaiface.h)
description: The GetMulticastMode method retrieves the multicast mode.
helpviewer_keywords: ["GetMulticastMode","GetMulticastMode method [Microsoft TV Technologies]","GetMulticastMode method [Microsoft TV Technologies]","IBDA_EthernetFilter interface","IBDA_EthernetFilter interface [Microsoft TV Technologies]","GetMulticastMode method","IBDA_EthernetFilter.GetMulticastMode","IBDA_EthernetFilter::GetMulticastMode","IBDA_EthernetFilterGetMulticastMode","bdaiface/IBDA_EthernetFilter::GetMulticastMode","mstv.ibda_ethernetfilter_getmulticastmode"]
old-location: mstv\ibda_ethernetfilter_getmulticastmode.htm
tech.root: mstv
ms.assetid: 8a0a5dbb-642a-458b-a5b2-80e993ab61ca
ms.date: 12/05/2018
ms.keywords: GetMulticastMode, GetMulticastMode method [Microsoft TV Technologies], GetMulticastMode method [Microsoft TV Technologies],IBDA_EthernetFilter interface, IBDA_EthernetFilter interface [Microsoft TV Technologies],GetMulticastMode method, IBDA_EthernetFilter.GetMulticastMode, IBDA_EthernetFilter::GetMulticastMode, IBDA_EthernetFilterGetMulticastMode, bdaiface/IBDA_EthernetFilter::GetMulticastMode, mstv.ibda_ethernetfilter_getmulticastmode
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
 - IBDA_EthernetFilter::GetMulticastMode
 - bdaiface/IBDA_EthernetFilter::GetMulticastMode
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
 - IBDA_EthernetFilter.GetMulticastMode
---

# IBDA_EthernetFilter::GetMulticastMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMulticastMode</b> method retrieves the multicast mode.

## -parameters

### -param pulModeMask [out]

Pointer that receives the multicast mode.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

See the Windows DDK for possible values.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ethernetfilter">IBDA_EthernetFilter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ethernetfilter-putmulticastmode">PutMulticastMode</a>