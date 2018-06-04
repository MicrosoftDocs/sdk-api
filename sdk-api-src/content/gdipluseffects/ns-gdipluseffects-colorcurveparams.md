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

# ColorCurveParams structure


## -description


A <b>ColorCurveParams</b> structure contains members that specify an adjustment to the colors of a bitmap.

The <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>ColorCurveParams</b> structure.</li>
<li>Pass the address of the <b>ColorCurveParams</b> structure to the <a href="https://msdn.microsoft.com/9e523edd-324d-473a-8a3b-36d99f4327ee">ColorCurve::SetParameters</a> method of a <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field adjustment

Type: <b><a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">CurveAdjustments</a></b>

Element of the <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">CurveAdjustments</a> enumeration that specifies the adjustment to be applied.


### -field channel

Type: <b><a href="https://msdn.microsoft.com/fc85749e-d94e-45b9-b2c3-b45bd19f4b09">CurveChannel</a></b>

Element of the <a href="https://msdn.microsoft.com/fc85749e-d94e-45b9-b2c3-b45bd19f4b09">CurveChannel</a> enumeration that specifies the color channel to which the adjustment applies.


### -field adjustValue

Type: <b>INT</b>

Integer that specifies the intensity of the adjustment. The range of acceptable values depends on which adjustment is being applied. To see the range of acceptable values for a particular adjustment, see the <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">CurveAdjustments</a> enumeration.

