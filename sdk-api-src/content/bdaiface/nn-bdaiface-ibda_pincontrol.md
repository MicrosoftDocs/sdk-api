---
UID: NN:bdaiface.IBDA_PinControl
title: IBDA_PinControl (bdaiface.h)
description: The IBDA_PinControl interface is exposed on a BDA device filter's pins. A Network Provider calls these methods to determine the type and identifier of each pin on the filter. A Network Provider uses this information when building the graph.
helpviewer_keywords: ["IBDA_PinControl","IBDA_PinControl interface [Microsoft TV Technologies]","IBDA_PinControl interface [Microsoft TV Technologies]","described","IBDA_PinControlInterface","bdaiface/IBDA_PinControl","mstv.ibda_pincontrol"]
old-location: mstv\ibda_pincontrol.htm
tech.root: mstv
ms.assetid: 2d318cc4-b3f2-4fb6-b9e3-8ba8312ad2ae
ms.date: 12/05/2018
ms.keywords: IBDA_PinControl, IBDA_PinControl interface [Microsoft TV Technologies], IBDA_PinControl interface [Microsoft TV Technologies],described, IBDA_PinControlInterface, bdaiface/IBDA_PinControl, mstv.ibda_pincontrol
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
 - IBDA_PinControl
 - bdaiface/IBDA_PinControl
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
 - IBDA_PinControl
---

# IBDA_PinControl interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_PinControl</b> interface is exposed on a BDA device filter's pins. A Network Provider calls these methods to determine the type and identifier of each pin on the filter. A Network Provider uses this information when building the graph.

## -inheritance

The <b>IBDA_PinControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_PinControl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_PinControl)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
