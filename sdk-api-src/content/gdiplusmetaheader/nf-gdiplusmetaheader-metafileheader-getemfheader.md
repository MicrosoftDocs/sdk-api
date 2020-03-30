---
UID: NF:gdiplusmetaheader.MetafileHeader.GetEmfHeader
title: MetafileHeader::GetEmfHeader (gdiplusmetaheader.h)
description: The MetafileHeader::GetEmfHeader method gets an ENHMETAHEADER3 structure that contains properties of the associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetEmfHeader_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getemfheader.htm
ms.date: 12/05/2018
ms.keywords: GetEmfHeader, GetEmfHeader method [GDI+], GetEmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetEmfHeader method, MetafileHeader.GetEmfHeader, MetafileHeader::GetEmfHeader, _gdiplus_CLASS_MetafileHeader_GetEmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetEmfHeader_
f1_keywords:
- gdiplusmetaheader/MetafileHeader.GetEmfHeader
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- MetafileHeader.GetEmfHeader
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# MetafileHeader::GetEmfHeader


## -description


The <b>MetafileHeader::GetEmfHeader</b> method gets an <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a>*</b>

If the associated metafile is in the EMF or EMF+ format, this method returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a> structure that contains properties of the associated metafile. If the associated metafile is in the WMF format, this method returns <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a>



<a href="https://docs.microsoft.com/previous-versions/ms535280(v=vs.85)">GetMetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
 

 

