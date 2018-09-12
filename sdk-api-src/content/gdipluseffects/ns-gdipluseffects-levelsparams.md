---
UID: NS:gdipluseffects.LevelsParams
title: LevelsParams
author: windows-sdk-content
description: The LevelsParams structure contains members that specify adjustments to the light, midtone, or dark areas of a bitmap.
old-location: gdiplus\_gdiplus_STRUC_LevelsParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\levelsparams.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: LevelsParams, LevelsParams structure [GDI+], _gdiplus_STRUC_LevelsParams, gdiplus._gdiplus_STRUC_LevelsParams, gdipluseffects/LevelsParams
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
 - LevelsParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# LevelsParams structure


## -description


The <b>LevelsParams</b> structure contains members that specify adjustments to the light, midtone, or dark areas of a bitmap.

You can adjust the light, midtone, or dark areas of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>LevelsParams</b> structure.</li>
<li>Pass the address of the <b>LevelsParams</b> structure to the <a href="https://msdn.microsoft.com/928f88d3-1fc0-49a5-b286-794c157d10aa">Levels::SetParameters</a> method of a <a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field highlight

Type: <b>INT</b>

Integer in the range 0 through 100 that specifies which pixels should be lightened. You can use this adjustment to lighten pixels that are already lighter than a certain threshold. Setting <b>highlight</b> to 100 specifies no change. Setting <b>highlight</b> to t specifies that a color channel value is increased if it is already greater than t percent of full intensity. For example, setting <b>highlight</b> to 90 specifies that all color channel values greater than 90 percent of full intensity are increased.


### -field midtone

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies how much to lighten or darken an image. Color channel values in the middle of the intensity range are altered more than color channel values near the minimum or maximum intensity. You can use this adjustment to lighten (or darken) an image without loosing the contrast between the darkest and lightest portions of the image. A value of 0 specifies no change. Positive values specify that the midtones are made lighter, and negative values specify that the midtones are made darker. 


### -field shadow

Type: <b>INT</b>

Integer in the range 0 through 100 that specifies which pixels should be darkened. You can use this adjustment to darken pixels that are already darker than a certain threshold. Setting <b>shadow</b> to 0 specifies no change. Setting <b>shadow</b> to t specifies that a color channel value is decreased if it is already less than t percent of full intensity. For example, setting <b>shadow</b> to 10 specifies that all color channel values less than 10 percent of full intensity are decreased.

