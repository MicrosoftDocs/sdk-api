---
UID: NF:gdiplusheaders.Metafile.GetMetafileHeader(IN const WCHAR,OUT MetafileHeader)
title: Metafile::GetMetafileHeader(IN const WCHAR,OUT MetafileHeader) (gdiplusheaders.h)
description: The Metafile::GetMetafileHeader method gets the header.helpviewer_keywords: ["GetMetafileHeader","GetMetafileHeader method [GDI+]","GetMetafileHeader method [GDI+]","Metafile class","Metafile class [GDI+]","GetMetafileHeader method","Metafile.GetMetafileHeader","Metafile.GetMetafileHeader(IN const WCHAR","OUT MetafileHeader)","Metafile.GetMetafileHeader(const WCHAR*","MetafileHeader*)","Metafile::GetMetafileHeader","Metafile::GetMetafileHeader(IN const WCHAR","OUT MetafileHeader)","_gdiplus_CLASS_Metafile_GetMetafileHeader_filename_header_","gdiplus._gdiplus_CLASS_Metafile_GetMetafileHeader_filename_header_"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_GetMetafileHeader_filename_header_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\metafilegetmetafileheadermethods\getmetafileheader.htm
ms.date: 12/05/2018
ms.keywords: GetMetafileHeader, GetMetafileHeader method [GDI+], GetMetafileHeader method [GDI+],Metafile class, Metafile class [GDI+],GetMetafileHeader method, Metafile.GetMetafileHeader, Metafile.GetMetafileHeader(IN const WCHAR,OUT MetafileHeader), Metafile.GetMetafileHeader(const WCHAR*,MetafileHeader*), Metafile::GetMetafileHeader, Metafile::GetMetafileHeader(IN const WCHAR,OUT MetafileHeader), _gdiplus_CLASS_Metafile_GetMetafileHeader_filename_header_, gdiplus._gdiplus_CLASS_Metafile_GetMetafileHeader_filename_header_
f1_keywords:
- gdiplusheaders/Metafile.GetMetafileHeader
dev_langs:
- c++
req.header: gdiplusheaders.h
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
- Metafile.GetMetafileHeader
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Metafile::GetMetafileHeader(IN const WCHAR,OUT MetafileHeader)


## -description


The <b>Metafile::GetMetafileHeader</b> method gets the header.


## -parameters




### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of an existing 

					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object that contains the header. 


### -param header [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a> object that receives the header, which contains the attributes of the metafile. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns OK, which is an element of the 

						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
 

 

