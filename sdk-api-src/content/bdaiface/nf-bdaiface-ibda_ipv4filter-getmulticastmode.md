---
UID: NF:bdaiface.IBDA_IPV4Filter.GetMulticastMode
title: IBDA_IPV4Filter::GetMulticastMode (bdaiface.h)
description: The GetMulticastMode method retrieves the multicast mode.
helpviewer_keywords: ["GetMulticastMode","GetMulticastMode method [Microsoft TV Technologies]","GetMulticastMode method [Microsoft TV Technologies]","IBDA_IPV4Filter interface","IBDA_IPV4Filter interface [Microsoft TV Technologies]","GetMulticastMode method","IBDA_IPV4Filter.GetMulticastMode","IBDA_IPV4Filter::GetMulticastMode","IBDA_IPV4FilterGetMulticastMode","bdaiface/IBDA_IPV4Filter::GetMulticastMode","mstv.ibda_ipv4filter_getmulticastmode"]
old-location: mstv\ibda_ipv4filter_getmulticastmode.htm
tech.root: mstv
ms.assetid: 231c20f6-3204-48a3-ad07-3df9c6d87bd7
ms.date: 12/05/2018
ms.keywords: GetMulticastMode, GetMulticastMode method [Microsoft TV Technologies], GetMulticastMode method [Microsoft TV Technologies],IBDA_IPV4Filter interface, IBDA_IPV4Filter interface [Microsoft TV Technologies],GetMulticastMode method, IBDA_IPV4Filter.GetMulticastMode, IBDA_IPV4Filter::GetMulticastMode, IBDA_IPV4FilterGetMulticastMode, bdaiface/IBDA_IPV4Filter::GetMulticastMode, mstv.ibda_ipv4filter_getmulticastmode
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
 - IBDA_IPV4Filter::GetMulticastMode
 - bdaiface/IBDA_IPV4Filter::GetMulticastMode
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
 - IBDA_IPV4Filter.GetMulticastMode
---

# IBDA_IPV4Filter::GetMulticastMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMulticastMode</b> method retrieves the multicast mode.

## -parameters

### -param pulModeMask [out]

Pointer that receives the mask. See the Windows DDK for possible values.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv4filter">IBDA_IPV4Filter Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_ipv4filter-putmulticastmode">PutMulticastMode</a>