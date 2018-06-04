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

# CurveAdjustments enumeration


## -description


The <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> class encompasses the eight bitmap adjustments listed in the <b>CurveAdjustments</b> enumeration.

To apply one of the eight adjustments to a bitmap, follow these steps.
<ol>
<li>Create a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure, and set its <b>adjustment</b> member to one of the elements of the <b>CurveAdjustments</b> enumeration.</li>
<li>Set the other two members (<b>adjustValue</b> and <b>channel</b>) of the <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> structure to the <a href="https://msdn.microsoft.com/9e523edd-324d-473a-8a3b-36d99f4327ee">ColorCurve::SetParameters</a> method of a <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -enum-fields




### -field AdjustExposure

Simulates increasing or decreasing the exposure of a photograph. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustExposure</a>, you should set the <b>adjustValue</b> member to an integer in the range -255 through 255. A value of 0 specifies no change in exposure. Positive values specify increased exposure and negative values specify decreased exposure.


### -field AdjustDensity

Simulates increasing or decreasing the film density of a photograph. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustDensity</a>, you should set the <b>adjustValue</b> member to an integer in the range -255 through 255. A value of 0 specifies no change in density. Positive values specify increased density (lighter picture) and negative values specify decreased density (darker picture).


### -field AdjustContrast

Increases or decreases the contrast of a bitmap. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustContrast</a>, you should set the <b>adjustValue</b> member to an integer in the range -100 through 100. A value of 0 specifies no change in contrast. Positive values specify increased contrast and negative values specify decreased contrast.


### -field AdjustHighlight

Increases or decreases the value of a color channel if that channel already has a value that is above half intensity. You can use this adjustment to get more definition in the light areas of an image without affecting the dark areas. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustHighlight</a>, you should set the <b>adjustValue</b> member to an integer in the range -100 through 100. A value of 0 specifies no change. Positive values specify that the light areas are made lighter, and negative values specify that the light areas are made darker.


### -field AdjustShadow

Increases or decreases the value of a color channel if that channel already has a value that is below half intensity. You can use this adjustment to get more definition in the dark areas of an image without affecting the light areas. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustShadow</a>, you should set the <b>adjustValue</b> member to an integer in the range -100 through 100. A value of 0 specifies no change. Positive values specify that the dark areas are made lighter, and negative values specify that the dark areas are made darker.


### -field AdjustMidtone

Lightens or darkens an image. Color channel values in the middle of the intensity range are altered more than color channel values near the minimum or maximum intensity. You can use this adjustment to lighten (or darken) an image without loosing the contrast between the darkest and lightest portions of the image. When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustMidtone</a>, you should set the <b>adjustValue</b> member to an integer in the range -100 through 100. A value of 0 specifies no change. Positive values specify that the midtones are made lighter, and negative values specify that the midtones are made darker.


### -field AdjustWhiteSaturation

When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustWhiteSaturation</a>, you should set the <b>adjustValue</b> member to an integer in the range 0 through 255. A value of t specifies that the interval [0, t] is mapped linearly to the interval [0, 255]. For example, if <b>adjustValue</b> is equal to 240, then color channel values in the interval [0, 240] are adjusted so that they spread out over the interval [0, 255]. Color channel values greater than 240 are set to 255.


### -field AdjustBlackSaturation

When you set the <b>adjustment</b> member of a <a href="https://msdn.microsoft.com/53204bea-b6b6-4a7c-a237-4754fbb92628">ColorCurveParams</a> object to <a href="https://msdn.microsoft.com/5c8ab5ba-242c-4d5d-a5d2-cf585b243856">AdjustBlackSaturation</a>, you should set the <b>adjustValue</b> member to an integer in the range 0 through 255. A value of t specifies that the interval [t, 255] is mapped linearly to the interval [0, 255]. For example, if <b>adjustValue</b> is equal to 15, then color channel values in the interval [15, 255] are adjusted so that they spread out over the interval [0, 255]. Color channel values less than 15 are set to 0.

