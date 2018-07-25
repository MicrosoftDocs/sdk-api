---
UID: NS:gdipluseffects.ColorLUTParams
title: ColorLUTParams
author: windows-sdk-content
description: A ColorLUTParams structure contains members (color lookup tables) that specify color adjustments to a bitmap.
old-location: gdiplus\_gdiplus_STRUC_ColorLUTParams.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorlutparams.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ColorLUTParams, ColorLUTParams structure [GDI+], _gdiplus_STRUC_ColorLUTParams, gdiplus._gdiplus_STRUC_ColorLUTParams, gdipluseffects/ColorLUTParams
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - ColorLUTParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ColorLUTParams structure


## -description


A <b>ColorLUTParams</b> structure contains members (color lookup tables) that specify color adjustments to a bitmap.

You can apply a custom adjustment to a bitmap by following these steps.
<ol>
<li>Create a <b>ColorLUTParams</b> structure.</li>
<li>Each member of the <b>ColorLUTParams</b> structure is a color lookup table (array of 256 bytes) for a particular color channel, alpha, red, green, or blue. Assign values of your choice to the four lookup tables.</li>
<li>Pass the address of the <b>ColorLUTParams</b> structure to the <a href="https://msdn.microsoft.com/94f35947-7e62-4f47-b21a-ed3939a4f36f">ColorLUT::SetParameters</a> method of a <a href="https://msdn.microsoft.com/d13dc185-e6f2-4a0f-b972-e9b6ce0859c6">ColorLUT</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/d13dc185-e6f2-4a0f-b972-e9b6ce0859c6">ColorLUT</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field lutB

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the blue channel.


### -field lutG

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the green channel.


### -field lutR

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the red channel.


### -field lutA

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the alpha channel.


## -remarks



A lookup table specifies how existing color channel values should be replaced by new values. A color channel value of j is replaced by the jth entry in the lookup table for that channel. For example, an existing blue channel value of 25 would be replaced by the value of lutB[25].

The ColorChannelLUT data type is defined in GdiplusColorMatrix.h as follows:

<code>typedef BYTE ColorChannelLUT[256];</code>



