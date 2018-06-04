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

# WICPngSrgbProperties enumeration


## -description


Specifies the Portable Network Graphics (PNG) sRGB chunk metadata properties.


## -enum-fields




### -field WICPngSrgbRenderingIntent

[VT_UI1] Indicates the rendering intent for an sRGB color space image. The rendering intents have the following meaning.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Perceptual</td>
</tr>
<tr>
<td>1</td>
<td>Relative colorimetric</td>
</tr>
<tr>
<td>2</td>
<td>Saturation</td>
</tr>
<tr>
<td>3</td>
<td>Absolute colorimetric</td>
</tr>
</table>
 


### -field WICPngSrgbProperties_FORCE_DWORD



