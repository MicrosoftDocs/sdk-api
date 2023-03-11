---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003
title: XPS_SPREAD_METHOD (xpsobjectmodel.h)
description: Describes how the spread region is to be filled.
helpviewer_keywords: ["XPS_SPREAD_METHOD","XPS_SPREAD_METHOD enumeration [XPS Documents and Packaging]","XPS_SPREAD_METHOD_PAD","XPS_SPREAD_METHOD_REFLECT","XPS_SPREAD_METHOD_REPEAT","xps.xps_spread_method","xpsobjectmodel/XPS_SPREAD_METHOD","xpsobjectmodel/XPS_SPREAD_METHOD_PAD","xpsobjectmodel/XPS_SPREAD_METHOD_REFLECT","xpsobjectmodel/XPS_SPREAD_METHOD_REPEAT"]
old-location: xps\xps_spread_method.htm
tech.root: xps
ms.assetid: 9c9cadaf-6f38-4a56-942e-78617017a905
ms.date: 12/05/2018
ms.keywords: XPS_SPREAD_METHOD, XPS_SPREAD_METHOD enumeration [XPS Documents and Packaging], XPS_SPREAD_METHOD_PAD, XPS_SPREAD_METHOD_REFLECT, XPS_SPREAD_METHOD_REPEAT, xps.xps_spread_method, xpsobjectmodel/XPS_SPREAD_METHOD, xpsobjectmodel/XPS_SPREAD_METHOD_PAD, xpsobjectmodel/XPS_SPREAD_METHOD_REFLECT, xpsobjectmodel/XPS_SPREAD_METHOD_REPEAT
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_SPREAD_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0003
 - XPS_SPREAD_METHOD
 - xpsobjectmodel/XPS_SPREAD_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_SPREAD_METHOD
---

# XPS_SPREAD_METHOD enumeration


## -description

Describes how the spread region is  to be filled. 
 The spread region is the area that falls within the drawing area but outside of the gradient region.

## -enum-fields

### -field XPS_SPREAD_METHOD_PAD:1

The spread region is filled with the color whose value equals the color  at the end of the gradient region.

### -field XPS_SPREAD_METHOD_REFLECT

The spread region is filled by repeating the alternating reflection of the gradient that is  inside the gradient region.

### -field XPS_SPREAD_METHOD_REPEAT

The spread region is filled by repeating the gradient that is inside the gradient region, in the same orientation and direction.

## -remarks

The following illustration shows the effect of the spread methods on gradients that are drawn by using the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a> and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a> interfaces. The gradient region of an <b>IXpsOMLinearGradientBrush</b> interface is defined by calling the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-setstartpoint">SetStartPoint</a> and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomlineargradientbrush-setendpoint">SetEndPoint</a> methods; the gradient region of an  <b>IXpsOMRadialGradientBrush</b> interface is defined by calling the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setcenter">SetCenter</a>, <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setgradientorigin">SetGradientOrigin</a>, and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomradialgradientbrush-setradiisizes">SetRadiiSizes</a>  methods.     The gradient region is the area inside the dashed lines, and the spread area is the area outside of the gradient region.

<img alt="An illustration that shows examples of the spread method" src="./images/XPS_Spread_Method.png"/>

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>
