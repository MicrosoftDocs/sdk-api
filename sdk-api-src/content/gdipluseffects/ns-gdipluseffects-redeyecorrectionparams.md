---
UID: NS:gdipluseffects.RedEyeCorrectionParams
title: RedEyeCorrectionParams
author: windows-sdk-content
description: A RedEyeCorrectionParams structure contains members that specify the areas of a bitmap to which a red-eye correction is applied.
old-location: gdiplus\_gdiplus_STRUC_RedEyeCorrectionParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\redeyecorrectionparams.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: RedEyeCorrectionParams, RedEyeCorrectionParams structure [GDI+], _gdiplus_STRUC_RedEyeCorrectionParams, gdiplus._gdiplus_STRUC_RedEyeCorrectionParams, gdipluseffects/RedEyeCorrectionParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - RedEyeCorrectionParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
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

Integer that specifies the number of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures in the <b>areas</b> array.


### -field areas

Type: <b>RECT*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures, each of which specifies an area of the bitmap to which red eye correction should be applied.

