---
UID: NS:gdipluseffects.TintParams
title: TintParams
author: windows-sdk-content
description: A TintParams structure contains members that specify the nature of a tint adjustment to a bitmap.
old-location: gdiplus\_gdiplus_STRUC_TintParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\tintparams.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: TintParams, TintParams structure [GDI+], _gdiplus_STRUC_TintParams, gdiplus._gdiplus_STRUC_TintParams, gdipluseffects/TintParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - TintParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
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

