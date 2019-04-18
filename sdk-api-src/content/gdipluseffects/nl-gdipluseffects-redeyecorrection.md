---
UID: NL:gdipluseffects.RedEyeCorrection
title: RedEyeCorrection (gdipluseffects.h)
author: windows-sdk-content
description: The RedEyeCorrection class enables you to correct the red eyes that sometimes occur in flash photographs.
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrection.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RedEyeCorrection, RedEyeCorrection class [GDI+], RedEyeCorrection class [GDI+],described, _gdiplus_CLASS_RedEyeCorrection_Class, gdiplus._gdiplus_CLASS_RedEyeCorrection_Class, gdipluseffects/RedEyeCorrection
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
ms.custom: 19H1
---

# RedEyeCorrection class


## -description


The <b>RedEyeCorrection</b> class enables you to correct the red eyes that sometimes occur in flash photographs. Pass the address of a <b>RedEyeCorrection</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify areas of the bitmap that have red eyes, pass a <a href="https://msdn.microsoft.com/en-us/library/ms534072(v=VS.85).aspx">RedEyeCorrectionParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms534928(v=VS.85).aspx">RedEyeCorrection::SetParameters</a> method of a <b>RedEyeCorrection</b> object.

