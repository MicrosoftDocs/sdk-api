---
UID: NL:gdipluseffects.Blur
title: Blur
author: windows-sdk-content
description: The Blur class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur.
old-location: gdiplus\_gdiplus_CLASS_Blur_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blur.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Blur, Blur class [GDI+], Blur class [GDI+],described, _gdiplus_CLASS_Blur_Class, gdiplus._gdiplus_CLASS_Blur_Class, gdipluseffects/Blur
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Blur
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Blur class


## -description


The <b>Blur</b> class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur. Pass the address of a <b>Blur</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the nature of the blur, pass a <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a> structure to the <a href="https://msdn.microsoft.com/d5e62587-01f3-4869-a596-7e84d1752e37">Blur::SetParameters</a> method of a <b>Blur</b> object.
		

