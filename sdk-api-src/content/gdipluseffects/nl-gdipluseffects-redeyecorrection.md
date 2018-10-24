---
UID: NL:gdipluseffects.RedEyeCorrection
title: RedEyeCorrection
author: windows-sdk-content
description: The RedEyeCorrection class enables you to correct the red eyes that sometimes occur in flash photographs.
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrection.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: RedEyeCorrection, RedEyeCorrection class [GDI+], RedEyeCorrection class [GDI+],described, _gdiplus_CLASS_RedEyeCorrection_Class, gdiplus._gdiplus_CLASS_RedEyeCorrection_Class, gdipluseffects/RedEyeCorrection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdipluseffects.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - RedEyeCorrection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RedEyeCorrection class


## -description


The <b>RedEyeCorrection</b> class enables you to correct the red eyes that sometimes occur in flash photographs. Pass the address of a <b>RedEyeCorrection</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify areas of the bitmap that have red eyes, pass a <a href="https://msdn.microsoft.com/5c4832f7-de89-4596-915f-2cd23b8c1c2f">RedEyeCorrectionParams</a> structure to the <a href="https://msdn.microsoft.com/ed889acb-37c1-4fa6-9c46-1f41428b9b36">RedEyeCorrection::SetParameters</a> method of a <b>RedEyeCorrection</b> object.

