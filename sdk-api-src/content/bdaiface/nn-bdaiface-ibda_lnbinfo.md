---
UID: NN:bdaiface.IBDA_LNBInfo
title: IBDA_LNBInfo (bdaiface.h)
description: The IBDA_LNBInfo interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.
helpviewer_keywords: ["IBDA_LNBInfo","IBDA_LNBInfo interface [Microsoft TV Technologies]","IBDA_LNBInfo interface [Microsoft TV Technologies]","described","IBDA_LNBInfoInterface","bdaiface/IBDA_LNBInfo","mstv.ibda_lnbinfo"]
old-location: mstv\ibda_lnbinfo.htm
tech.root: mstv
ms.assetid: 4985b525-c000-4d19-9679-c995cbc3c99b
ms.date: 12/05/2018
ms.keywords: IBDA_LNBInfo, IBDA_LNBInfo interface [Microsoft TV Technologies], IBDA_LNBInfo interface [Microsoft TV Technologies],described, IBDA_LNBInfoInterface, bdaiface/IBDA_LNBInfo, mstv.ibda_lnbinfo
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
 - IBDA_LNBInfo
 - bdaiface/IBDA_LNBInfo
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
 - IBDA_LNBInfo
---

# IBDA_LNBInfo interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_LNBInfo</b> interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.

## -inheritance

The <b>IBDA_LNBInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_LNBInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_LNBInfo)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
