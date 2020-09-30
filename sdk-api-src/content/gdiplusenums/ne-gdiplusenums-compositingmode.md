---
UID: NE:gdiplusenums.CompositingMode
title: CompositingMode (gdiplusenums.h)
description: The CompositingMode enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the Graphics::GetCompositingMode and Graphics::SetCompositingMode methods of the Graphics class.
helpviewer_keywords: ["CompositingMode","CompositingMode enumeration [GDI+]","CompositingModeSourceCopy","CompositingModeSourceOver","_gdiplus_ENUM_CompositingMode","gdiplus._gdiplus_ENUM_CompositingMode","gdiplusenums/CompositingMode","gdiplusenums/CompositingModeSourceCopy","gdiplusenums/CompositingModeSourceOver"]
old-location: gdiplus\_gdiplus_ENUM_CompositingMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\compositingmode.htm
ms.date: 12/05/2018
ms.keywords: CompositingMode, CompositingMode enumeration [GDI+], CompositingModeSourceCopy, CompositingModeSourceOver, _gdiplus_ENUM_CompositingMode, gdiplus._gdiplus_ENUM_CompositingMode, gdiplusenums/CompositingMode, gdiplusenums/CompositingModeSourceCopy, gdiplusenums/CompositingModeSourceOver
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - CompositingMode
 - gdiplusenums/CompositingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - CompositingMode
---

# CompositingMode enumeration


## -description

The <b>CompositingMode</b> enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingmode">Graphics::GetCompositingMode</a> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode">Graphics::SetCompositingMode</a> methods of the 
			<b>Graphics</b> class.

## -enum-fields

### -field CompositingModeSourceOver

Specifies that when a color is rendered, it is blended with the background color. The blend is determined by the alpha component of the color being rendered.

### -field CompositingModeSourceCopy

Specifies that when a color is rendered, it overwrites the background color. This mode cannot be used along with TextRenderingHintClearTypeGridFit.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingmode">Graphics::GetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode">Graphics::SetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-textrenderinghint">TextRenderingHint</a>