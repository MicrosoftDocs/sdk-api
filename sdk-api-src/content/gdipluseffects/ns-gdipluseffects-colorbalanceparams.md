---
UID: NS:gdipluseffects.ColorBalanceParams
title: ColorBalanceParams
author: windows-sdk-content
description: A ColorBalanceParams structure contains members that specify the nature of a color balance adjustment.
old-location: gdiplus\_gdiplus_STRUC_ColorBalanceParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorbalanceparams.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ColorBalanceParams, ColorBalanceParams structure [GDI+], _gdiplus_STRUC_ColorBalanceParams, gdiplus._gdiplus_STRUC_ColorBalanceParams, gdipluseffects/ColorBalanceParams
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
 - ColorBalanceParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ColorBalanceParams structure


## -description


A <b>ColorBalanceParams</b> structure contains members that specify the nature of a color balance adjustment.

You can change the color balance of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>ColorBalanceParams</b> structure.</li>
<li>Pass the address of the <b>ColorBalanceParams</b> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536264(v=VS.85).aspx">ColorBalance::SetParameters</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534428(v=VS.85).aspx">ColorBalance</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534428(v=VS.85).aspx">ColorBalance</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field cyanRed

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of red in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of red in the image increases and the amount of cyan decreases. As the value moves from 0 to -100, the amount of red in the image decreases and the amount of cyan increases.


### -field magentaGreen

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of green in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of green in the image increases and the amount of magenta decreases. As the value moves from 0 to -100, the amount of green in the image decreases and the amount of magenta increases.


### -field yellowBlue

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of blue in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of blue in the image increases and the amount of yellow decreases. As the value moves from 0 to -100, the amount of blue in the image decreases and the amount of yellow increases.

