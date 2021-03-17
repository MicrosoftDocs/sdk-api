---
UID: NF:gdiplusgraphics.Graphics.AddMetafileComment
title: Graphics::AddMetafileComment (gdiplusgraphics.h)
description: The Graphics::AddMetafileComment method adds a text comment to an existing metafile.
helpviewer_keywords: ["AddMetafileComment","AddMetafileComment method [GDI+]","AddMetafileComment method [GDI+]","Graphics class","Graphics class [GDI+]","AddMetafileComment method","Graphics.AddMetafileComment","Graphics::AddMetafileComment","_gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_","gdiplus._gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\addmetafilecomment.htm
ms.date: 12/05/2018
ms.keywords: AddMetafileComment, AddMetafileComment method [GDI+], AddMetafileComment method [GDI+],Graphics class, Graphics class [GDI+],AddMetafileComment method, Graphics.AddMetafileComment, Graphics::AddMetafileComment, _gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_, gdiplus._gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_
req.header: gdiplusgraphics.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::AddMetafileComment
 - gdiplusgraphics/Graphics::AddMetafileComment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.AddMetafileComment
---

# Graphics::AddMetafileComment


## -description

The <b>Graphics::AddMetafileComment</b> method adds a text comment to an existing metafile.

## -parameters

### -param data [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that contains the comment.

### -param sizeData [in]

Type: <b>UINT</b>

Integer that specifies the number of bytes in the value of the 
					<i>data</i> parameter.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>