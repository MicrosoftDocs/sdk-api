---
UID: NF:gdiplusmetaheader.MetafileHeader.GetWmfHeader
title: MetafileHeader::GetWmfHeader (gdiplusmetaheader.h)
description: The MetafileHeader::GetWmfHeader method gets a METAHEADER structure that contains properties of the associated metafile.
helpviewer_keywords: ["GetWmfHeader","GetWmfHeader method [GDI+]","GetWmfHeader method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","GetWmfHeader method","MetafileHeader.GetWmfHeader","MetafileHeader::GetWmfHeader","_gdiplus_CLASS_MetafileHeader_GetWmfHeader_","gdiplus._gdiplus_CLASS_MetafileHeader_GetWmfHeader_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetWmfHeader_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getwmfheader.htm
ms.date: 12/05/2018
ms.keywords: GetWmfHeader, GetWmfHeader method [GDI+], GetWmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetWmfHeader method, MetafileHeader.GetWmfHeader, MetafileHeader::GetWmfHeader, _gdiplus_CLASS_MetafileHeader_GetWmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetWmfHeader_
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
 - MetafileHeader::GetWmfHeader
 - gdiplusmetaheader/MetafileHeader::GetWmfHeader
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
 - MetafileHeader.GetWmfHeader
---

# MetafileHeader::GetWmfHeader


## -description

The <b>MetafileHeader::GetWmfHeader</b> method gets a <a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a> structure that contains properties of the associated metafile.



## -returns

Type: <b><a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a>*</b>

If the associated metafile is in the WMF format, this method returns a pointer to a structure that contains properties of the associated metafile. If the associated metafile is in the EMF or EMF+ format, this method returns <b>NULL</b>. The <a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a> structure is defined in Wingdi.h.

## -see-also

<a href="/previous-versions/ms535280(v=vs.85)">GetMetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
