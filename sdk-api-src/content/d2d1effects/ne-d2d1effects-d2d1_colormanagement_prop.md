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

# D2D1_COLORMANAGEMENT_PROP enumeration


## -description



          Identifiers for the properties of the <a href="https://msdn.microsoft.com/7351C4B4-F289-4236-BB42-1B3BD8753248">Color management effect</a>.
        


## -enum-fields




### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT

The source color space information. 
          

The type is <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>.

The default value is NULL.


### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT

Which ICC rendering intent to use. 
          

The type is <a href="https://msdn.microsoft.com/64161335-7974-4B8D-9385-045A94625FE1">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.


### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT

The destination color space information. 
          

The type is <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>.

The default value is NULL.


### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT

Which ICC rendering intent to use. 
          

The type is <a href="https://msdn.microsoft.com/64161335-7974-4B8D-9385-045A94625FE1">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.


### -field D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE

How to interpret alpha data that is contained in the input image. 
          

The type is <a href="https://msdn.microsoft.com/CEC066A7-085E-4657-B9CF-9F8B8E8F4FFE">D2D1_COLORMANAGEMENT_ALPHA_MODE</a>.

The default value is D2D1_COLORMANAGEMENT_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_COLORMANAGEMENT_PROP_QUALITY

The quality level of the transform. 
          

The type is <a href="https://msdn.microsoft.com/99BB95AE-E5C6-4D56-9EB9-740DD7D0EFEF">D2D1_COLORMANAGEMENT_QUALITY</a>.

The default value is D2D1_COLORMANAGEMENT_QUALITY_NORMAL.


### -field D2D1_COLORMANAGEMENT_PROP_FORCE_DWORD



