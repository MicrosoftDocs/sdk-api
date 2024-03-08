---
UID: NN:bdaiface.ICCSubStreamFiltering
title: ICCSubStreamFiltering (bdaiface.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["ICCSubStreamFiltering","ICCSubStreamFiltering interface [Microsoft TV Technologies]","ICCSubStreamFiltering interface [Microsoft TV Technologies]","described","ICCSubStreamFilteringInterface","bdaiface/ICCSubStreamFiltering","mstv.iccsubstreamfiltering"]
old-location: mstv\iccsubstreamfiltering.htm
tech.root: mstv
ms.assetid: 2de6796d-beb3-4611-a559-449fe21193a6
ms.date: 12/05/2018
ms.keywords: ICCSubStreamFiltering, ICCSubStreamFiltering interface [Microsoft TV Technologies], ICCSubStreamFiltering interface [Microsoft TV Technologies],described, ICCSubStreamFilteringInterface, bdaiface/ICCSubStreamFiltering, mstv.iccsubstreamfiltering
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
 - ICCSubStreamFiltering
 - bdaiface/ICCSubStreamFiltering
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
 - ICCSubStreamFiltering
---

# ICCSubStreamFiltering interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>ICCSubStreamFiltering</b> interface sets the filtering on the closed captioning (CC) pins of the <a href="/previous-versions/windows/desktop/mstv/vbicodec-filter">VBICodec</a> filter. The CC output pins on the VBICodec filter both expose this interface. Use this interface to select which CC services are delivered by each pin. The CC pins are independent, so you can select different services on each pin. For example, you might select CC1 and CC2 on one pin and extended data services (XDS) on the other.

## -inheritance

The <b>ICCSubStreamFiltering</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICCSubStreamFiltering</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ICCSubStreamFiltering)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
