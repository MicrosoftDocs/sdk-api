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

# D2D1_EDGEDETECTION_PROP enumeration


## -description


Identifiers for properties of the Edge Detection effect.


## -enum-fields




### -field D2D1_EDGEDETECTION_PROP_STRENGTH

The D2D1_EDGEDETECTION_PROP_STRENGTH property is a float value modulating the response of the edge detection filter. A low strength value means that weaker edges will get filtered out, 
          while a high value means stronger edges will get filtered out.  The allowed range is 0.0 to 1.0.  The default value is 0.5.


### -field D2D1_EDGEDETECTION_PROP_BLUR_RADIUS

The D2D1_EDGEDETECTION_PROP_BLUR_RADIUS property is a float value specifying the amount of blur to apply.  Applying blur is used to remove high frequencies and reduce phantom edges.  
          The allowed range is 0.0 to 10.0. The default value is 0.0 (no blur applied).


### -field D2D1_EDGEDETECTION_PROP_MODE

The D2D1_EDGEDETECTION_PROP_MODE property is a <a href="https://msdn.microsoft.com/22C57518-8617-44F3-BC04-42605A77985C">D2D1_EDGEDETECTION_MODE</a> enumeration value which mode to use for edge detection.  
          The default value is D2D1_EDGEDETECTION_MODE_SOBEL.


### -field D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES

The D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES property is a boolean value. Edge detection only applies to the RGB channels, the alpha channel is ignored for purposes of detecting edges.
          If D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES is false, the output edges is fully opaque. If D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES is true, the input opacity is preserved.
          The default value is false.


### -field D2D1_EDGEDETECTION_PROP_ALPHA_MODE

The D2D1_EDGEDETECTION_PROP_ALPHA_MODE property is a <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a> enumeration value indicating the alpha mode of the input file.
          If the input is not opaque, this value is used to determine whether to unpremultiply the inputs.
          See the About Alpha Modes section of the <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a> topic for additional information.   
          
          The default value is D2D1_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_EDGEDETECTION_PROP_FORCE_DWORD



