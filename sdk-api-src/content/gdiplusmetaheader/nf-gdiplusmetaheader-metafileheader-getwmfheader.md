---
UID: NF:gdiplusmetaheader.MetafileHeader.GetWmfHeader
title: MetafileHeader::GetWmfHeader (gdiplusmetaheader.h)
description: The MetafileHeader::GetWmfHeader method gets a METAHEADER structure that contains properties of the associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetWmfHeader_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getwmfheader.htm
ms.date: 12/05/2018
ms.keywords: GetWmfHeader, GetWmfHeader method [GDI+], GetWmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetWmfHeader method, MetafileHeader.GetWmfHeader, MetafileHeader::GetWmfHeader, _gdiplus_CLASS_MetafileHeader_GetWmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetWmfHeader_
ms.topic: method
f1_keywords:
- gdiplusmetaheader/MetafileHeader.GetWmfHeader
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
- MetafileHeader.GetWmfHeader
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# MetafileHeader::GetWmfHeader


## -description


The <b>MetafileHeader::GetWmfHeader</b> method gets a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a> structure that contains properties of the associated metafile.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a>*</b>
</strong>

If the associated metafile is in the WMF format, this method returns a pointer to a structure that contains properties of the associated metafile. If the associated metafile is in the EMF or EMF+ format, this method returns <b>NULL</b>. The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a> structure is defined in Wingdi.h.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/ms535280(v=vs.85)">GetMetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
 

 

