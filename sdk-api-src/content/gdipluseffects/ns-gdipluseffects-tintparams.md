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

# TintParams structure


## -description


A <b>TintParams</b> structure contains members that specify the nature of a tint adjustment to a bitmap.

You can adjust the tint of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>TintParams</b> structure.</li>
<li>Pass the address of the <b>TintParams</b> structure to the <a href="https://msdn.microsoft.com/f1d19fc2-2912-47f9-aa6b-29ae8df64a90">Tint::SetParameters</a> method of a <a href="https://msdn.microsoft.com/f012ec61-986d-40f4-a730-1b73a52952a8">Tint</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/f012ec61-986d-40f4-a730-1b73a52952a8">Tint</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field hue

Type: <b>INT</b>

Integer in the range -180 through 180 that specifies the hue to be strengthened or weakened. A value of 0 specifies blue. A positive value specifies a clockwise angle on the color wheel. For example, positive 60 specifies cyan and positive 120 specifies green. A negative value specifies a counter-clockwise angle on the color wheel. For example, negative 60 specifies magenta and negative 120 specifies red.


### -field amount

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies how much the hue (given by the <b>hue</b> parameter) is strengthened or weakened. A value of 0 specifies no change. Positive values specify that the hue is strengthened and negative values specify that the hue is weakened.

