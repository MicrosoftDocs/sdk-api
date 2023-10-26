---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020
title: XPS_DASH (xpsobjectmodel.h)
description: This structure describes a dash element of a path.
helpviewer_keywords: ["XPS_DASH","XPS_DASH structure [XPS Documents and Packaging]","xps.xps_dash","xpsobjectmodel/XPS_DASH"]
old-location: xps\xps_dash.htm
tech.root: xps
ms.assetid: c8f43f91-eefb-4025-8042-c2601e89d315
ms.date: 12/05/2018
ms.keywords: XPS_DASH, XPS_DASH structure [XPS Documents and Packaging], xps.xps_dash, xpsobjectmodel/XPS_DASH
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
req.typenames: XPS_DASH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020
 - XPS_DASH
 - xpsobjectmodel/XPS_DASH
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
 - XPS_DASH
---

# XPS_DASH structure


## -description

This structure describes a dash element of a path.

## -struct-fields

### -field length

Length of the visible segment of the dash element.

### -field gap

Length of the space between the visible segments of the dash sequence.

## -remarks

The length must be non-negative and is measured in multiples of the path's stroke thickness.

 Values of <b>length</b> do not include the end caps of the visible segments.

The shape of the end caps of the visible segments is determined by the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a> value.

## -see-also

<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a>

