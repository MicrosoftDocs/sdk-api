---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024
title: XPS_COLOR (xpsobjectmodel.h)
description: The contents of the XPS_COLOR structure when the colorType is XPS_COLOR_TYPE_CONTEXT.
helpviewer_keywords: ["XPS_COLOR","XPS_COLOR structure [XPS Documents and Packaging]","XPS_COLOR_TYPE_CONTEXT","XPS_COLOR_TYPE_CONTEXT structure [XPS Documents and Packaging]","xps.xps_color_type_context","xpsobjectmodel/XPS_COLOR_TYPE_CONTEXT"]
old-location: xps\xps_color_type_context.htm
tech.root: xps
ms.assetid: 76dcabb0-2407-4877-9f52-100883746695
ms.date: 12/05/2018
ms.keywords: XPS_COLOR, XPS_COLOR structure [XPS Documents and Packaging], XPS_COLOR_TYPE_CONTEXT, XPS_COLOR_TYPE_CONTEXT structure [XPS Documents and Packaging], xps.xps_color_type_context, xpsobjectmodel/XPS_COLOR_TYPE_CONTEXT
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
req.typenames: XPS_COLOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024
 - XPS_COLOR
 - xpsobjectmodel/XPS_COLOR
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
 - XPS_COLOR
---

# XPS_COLOR structure


## -description

The contents of the <a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a> structure when the <i>colorType</i> is <b>XPS_COLOR_TYPE_CONTEXT</b>.

## -struct-fields

### -field colorType

### -field value

### -field value.sRGB

### -field value.sRGB.alpha

### -field value.sRGB.red

### -field value.sRGB.green

### -field value.sRGB.blue

### -field value.scRGB

### -field value.scRGB.alpha

### -field value.scRGB.red

### -field value.scRGB.green

### -field value.scRGB.blue

### -field value.context

### -field value.context.channelCount

### -field value.context.channels

### -field __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0028

 




#### - channelCount

The number of color channels, including the alpha channel.


#### - channels

An array of floating-point color values for up to nine color channels, including the alpha channel.

The first element in the array, <i>channels</i>[0], contains the value for the alpha channel. The remaining elements in the array have context-specific color channel values.

## -remarks

For information about how to interpret or apply the values in this structure's members, see the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>.

## -see-also

<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>