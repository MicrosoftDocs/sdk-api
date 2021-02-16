---
UID: NF:gdiplusheaders.Metafile.Metafile(HENHMETAFILE,BOOL)
title: Metafile::Metafile(IN HENHMETAFILE,IN BOOL) (gdiplusheaders.h)
description: Creates a Windows GDI+ Metafile::Metafile object for playback based on a Windows Graphics Device Interface (GDI) Enhanced Metafile (EMF) file.
helpviewer_keywords: ["Metafile","Metafile class [GDI+]","Metafile constructor","Metafile constructor [GDI+]","Metafile constructor [GDI+]","Metafile class","Metafile.Metafile","Metafile.Metafile(HENHMETAFILE","BOOL)","Metafile.Metafile(IN HENHMETAFILE","IN BOOL)","Metafile::Metafile","Metafile::Metafile(IN HENHMETAFILE","IN BOOL)","_gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_","gdiplus._gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_91hemf_deleteemf.htm
ms.date: 12/05/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(HENHMETAFILE,BOOL), Metafile.Metafile(IN HENHMETAFILE,IN BOOL), Metafile::Metafile, Metafile::Metafile(IN HENHMETAFILE,IN BOOL), _gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_, gdiplus._gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Metafile::Metafile
 - gdiplusheaders/Metafile::Metafile
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
 - Metafile.Metafile
---

# Metafile::Metafile(IN HENHMETAFILE,IN BOOL)


## -description

Creates a Windows GDI+ <b>Metafile::Metafile</b> object for playback based on a Windows Graphics Device Interface (GDI) Enhanced Metafile (EMF) file.

## -parameters

### -param hEmf [in]

Type: <b>HENHMETAFILE</b>

Windows handle to a metafile.

### -param deleteEmf [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the Windows handle to a metafile is deleted when the <b>Metafile::Metafile</b> object is deleted. <b>TRUE</b> specifies that the <i>hEmf</i> Windows handle is deleted, and <b>FALSE</b> specifies that the <i>hEmf</i> Windows handle is not deleted. The default value is <b>FALSE</b>.

## -remarks

This constructor allows GDI+ to own the windows handle to the metafile, which should not be used by other portions of your code until the <b>Metafile::Metafile</b> object is deleted or goes out of scope.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-gethenhmetafile">Metafile::GetHENHMETAFILE</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recording-metafiles-use">Recording Metafiles</a>