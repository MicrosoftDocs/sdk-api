---
UID: NL:gdipluseffects.ColorBalance
title: ColorBalance (gdipluseffects.h)
author: windows-sdk-content
description: The ColorBalance class enables you to change the color balance (relative amounts of red, green, and blue) of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_ColorBalance_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorbalance.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorBalance, ColorBalance class [GDI+], ColorBalance class [GDI+],described, _gdiplus_CLASS_ColorBalance_Class, gdiplus._gdiplus_CLASS_ColorBalance_Class, gdipluseffects/ColorBalance
ms.topic: class
f1_keywords: ["gdipluseffects/ColorBalance"]
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
 - ColorBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ColorBalance class


## -description


The <b>ColorBalance</b> class enables you to change the color balance (relative amounts of red, green, and blue) of a bitmap. Pass the address of a <b>ColorBalance</b> object to the <a href="https://docs.microsoft.com/previous-versions//ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the nature of the change, pass the address of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorbalanceparams">ColorBalanceParams</a> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorbalance-setparameters">ColorBalance::SetParameters</a> method of a <b>ColorBalance</b> object.

