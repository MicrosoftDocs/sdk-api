---
UID: NF:gdiplusmetaheader.MetafileHeader.IsEmfPlusDual
title: MetafileHeader::IsEmfPlusDual (gdiplusmetaheader.h)
description: The MetafileHeader::IsEmfPlusDual method determines whether the associated metafile is in the EMF+ Dual format.
helpviewer_keywords: ["IsEmfPlusDual","IsEmfPlusDual method [GDI+]","IsEmfPlusDual method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","IsEmfPlusDual method","MetafileHeader.IsEmfPlusDual","MetafileHeader::IsEmfPlusDual","_gdiplus_CLASS_MetafileHeader_IsEmfPlusDual_","gdiplus._gdiplus_CLASS_MetafileHeader_IsEmfPlusDual_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsEmfPlusDual_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\isemfplusdual.htm
ms.date: 12/05/2018
ms.keywords: IsEmfPlusDual, IsEmfPlusDual method [GDI+], IsEmfPlusDual method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsEmfPlusDual method, MetafileHeader.IsEmfPlusDual, MetafileHeader::IsEmfPlusDual, _gdiplus_CLASS_MetafileHeader_IsEmfPlusDual_, gdiplus._gdiplus_CLASS_MetafileHeader_IsEmfPlusDual_
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
 - MetafileHeader::IsEmfPlusDual
 - gdiplusmetaheader/MetafileHeader::IsEmfPlusDual
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
 - MetafileHeader.IsEmfPlusDual
---

# MetafileHeader::IsEmfPlusDual


## -description

The <b>MetafileHeader::IsEmfPlusDual</b> method determines whether the associated metafile is in the EMF+ Dual format.



## -returns

Type: <b>BOOL</b>

If the associated metafile is in the EMF+ Dual format, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. In particular, this method returns <b>FALSE</b> if the associated metafile is in the WMF, EMF, or EMF+ Only format.

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
