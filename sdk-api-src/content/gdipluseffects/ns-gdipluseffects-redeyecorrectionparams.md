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

# RedEyeCorrectionParams structure


## -description


A <b>RedEyeCorrectionParams</b> structure contains members that specify the areas of a bitmap to which a red-eye correction is applied.

You can can correct red eyes in a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>RedEyeCorrectionParams</b> structure.</li>
<li>Pass the address of the <b>RedEyeCorrectionParams</b> structure to the <a href="https://msdn.microsoft.com/ed889acb-37c1-4fa6-9c46-1f41428b9b36">RedEyeCorrection::SetParameters</a> method of a <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field numberOfAreas

Type: <b>UINT</b>

Integer that specifies the number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures in the <b>areas</b> array.


### -field areas

Type: <b>RECT*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures, each of which specifies an area of the bitmap to which red eye correction should be applied.

