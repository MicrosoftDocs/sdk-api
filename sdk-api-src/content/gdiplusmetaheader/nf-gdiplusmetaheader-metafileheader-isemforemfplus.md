---
UID: NF:gdiplusmetaheader.MetafileHeader.IsEmfOrEmfPlus
title: MetafileHeader::IsEmfOrEmfPlus (gdiplusmetaheader.h)
description: The MetafileHeader::IsEmfOrEmfPlus method determines whether the associated metafile is in either the EMF or EMF+ format.
helpviewer_keywords: ["IsEmfOrEmfPlus","IsEmfOrEmfPlus method [GDI+]","IsEmfOrEmfPlus method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","IsEmfOrEmfPlus method","MetafileHeader.IsEmfOrEmfPlus","MetafileHeader::IsEmfOrEmfPlus","_gdiplus_CLASS_MetafileHeader_IsEmfOrEmfPlus_","gdiplus._gdiplus_CLASS_MetafileHeader_IsEmfOrEmfPlus_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsEmfOrEmfPlus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\isemforemfplus.htm
ms.date: 12/05/2018
ms.keywords: IsEmfOrEmfPlus, IsEmfOrEmfPlus method [GDI+], IsEmfOrEmfPlus method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsEmfOrEmfPlus method, MetafileHeader.IsEmfOrEmfPlus, MetafileHeader::IsEmfOrEmfPlus, _gdiplus_CLASS_MetafileHeader_IsEmfOrEmfPlus_, gdiplus._gdiplus_CLASS_MetafileHeader_IsEmfOrEmfPlus_
req.header: gdiplusmetaheader.h
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
 - MetafileHeader::IsEmfOrEmfPlus
 - gdiplusmetaheader/MetafileHeader::IsEmfOrEmfPlus
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
 - MetafileHeader.IsEmfOrEmfPlus
---

# MetafileHeader::IsEmfOrEmfPlus


## -description

The <b>MetafileHeader::IsEmfOrEmfPlus</b> method determines whether the associated metafile is in either the EMF or EMF+ format.



## -returns

Type: <b>BOOL</b>

If the associated metafile is in the EMF or EMF+ format, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. In particular, this method returns <b>FALSE</b> if the associated metafile is in the WMF format.

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
