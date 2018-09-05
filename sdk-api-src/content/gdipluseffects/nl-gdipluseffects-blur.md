---
UID: NL:gdipluseffects.Blur
title: Blur
author: windows-sdk-content
description: The Blur class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur.
old-location: gdiplus\_gdiplus_CLASS_Blur_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blur.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Blur, Blur class [GDI+], Blur class [GDI+],described, _gdiplus_CLASS_Blur_Class, gdiplus._gdiplus_CLASS_Blur_Class, gdipluseffects/Blur
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdipluseffects.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Blur class


## -description


The <b>Blur</b> class enables you to apply a Gaussian blur effect to a bitmap and specify the nature of the blur. Pass the address of a <b>Blur</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the nature of the blur, pass a <a href="https://msdn.microsoft.com/34ad124d-8b12-4e9e-ae45-c2fd59baf3ff">BlurParams</a> structure to the <a href="https://msdn.microsoft.com/d5e62587-01f3-4869-a596-7e84d1752e37">Blur::SetParameters</a> method of a <b>Blur</b> object.
		

