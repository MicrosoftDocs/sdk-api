---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024"
author: windows-sdk-content
description: The contents of the XPS_COLOR structure when the colorType is XPS_COLOR_TYPE_CONTEXT.
old-location: xps\xps_color_type_context.htm
old-project: printdocs
ms.assetid: 76dcabb0-2407-4877-9f52-100883746695
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: XPS_COLOR, XPS_COLOR structure [XPS Documents and Packaging], XPS_COLOR_TYPE_CONTEXT, XPS_COLOR_TYPE_CONTEXT structure [XPS Documents and Packaging], __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024, xps.xps_color_type_context, xpsobjectmodel/XPS_COLOR_TYPE_CONTEXT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: XPS_COLOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_COLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0024 structure


## -description


The contents of the <a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a> structure when the <i>colorType</i> is <b>XPS_COLOR_TYPE_CONTEXT</b>.


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



For information about how to interpret or apply the values in this structure's members, see the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

