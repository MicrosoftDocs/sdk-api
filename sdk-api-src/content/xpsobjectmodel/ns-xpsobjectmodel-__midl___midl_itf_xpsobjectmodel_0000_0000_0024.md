---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

