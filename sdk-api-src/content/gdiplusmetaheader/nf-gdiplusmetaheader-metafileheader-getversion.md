---
UID: NF:gdiplusmetaheader.MetafileHeader.GetVersion
title: MetafileHeader::GetVersion (gdiplusmetaheader.h)
description: The MetafileHeader::GetVersion method gets the version of the metafile.
helpviewer_keywords: ["GetVersion","GetVersion method [GDI+]","GetVersion method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","GetVersion method","MetafileHeader.GetVersion","MetafileHeader::GetVersion","_gdiplus_CLASS_MetafileHeader_GetVersion_","gdiplus._gdiplus_CLASS_MetafileHeader_GetVersion_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetVersion_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getversion.htm
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [GDI+], GetVersion method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetVersion method, MetafileHeader.GetVersion, MetafileHeader::GetVersion, _gdiplus_CLASS_MetafileHeader_GetVersion_, gdiplus._gdiplus_CLASS_MetafileHeader_GetVersion_
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
 - MetafileHeader::GetVersion
 - gdiplusmetaheader/MetafileHeader::GetVersion
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
 - MetafileHeader.GetVersion
---

# MetafileHeader::GetVersion


## -description

The <b>MetafileHeader::GetVersion</b> method gets the version of the metafile.



## -returns

Type: <b>UINT</b>

This method returns the version of the metafile. The metafile version indicates whether the metafile is an EMF, EMF+, or WMF metafile. EMF files always have 0x0010000 as the version. EMF+ files currently have 0xdbc01001 as the version. WMF files usually have 0x0300 as the version; however, earlier versions may be 0x0100.

## -see-also

<a href="/previous-versions/ms535280(v=vs.85)">GetMetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
