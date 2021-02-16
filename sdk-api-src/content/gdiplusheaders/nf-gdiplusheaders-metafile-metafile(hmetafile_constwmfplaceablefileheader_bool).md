---
UID: NF:gdiplusheaders.Metafile.Metafile(HMETAFILE,constWmfPlaceableFileHeader,BOOL)
title: Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL) (gdiplusheaders.h)
description: Creates a Windows GDI+Metafile::Metafile object for recording. The format will be placeable metafile.
helpviewer_keywords: ["Metafile","Metafile class [GDI+]","Metafile constructor","Metafile constructor [GDI+]","Metafile constructor [GDI+]","Metafile class","Metafile.Metafile","Metafile.Metafile(HMETAFILE","const WmfPlaceableFileHeader*","BOOL)","Metafile.Metafile(IN HMETAFILE","IN const WmfPlaceableFileHeader","IN BOOL)","Metafile::Metafile","Metafile::Metafile(IN HMETAFILE","IN const WmfPlaceableFileHeader","IN BOOL)","_gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_","gdiplus._gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_34hwmf_wmfplaceablefileheader_deletewmf.htm
ms.date: 12/05/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(HMETAFILE,const WmfPlaceableFileHeader*,BOOL), Metafile.Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL), Metafile::Metafile, Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL), _gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_, gdiplus._gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_
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

# Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL)


## -description

Creates a Windows GDI+<b>Metafile::Metafile</b> object for recording. The format will be placeable metafile.

## -parameters

### -param hWmf [in]

Type: <b>HMETAFILE</b>

Windows handle to a metafile.

### -param wmfPlaceableFileHeader [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-wmfplaceablefileheader">WmfPlaceableFileHeader</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-wmfplaceablefileheader">WmfPlaceableFileHeader</a> structure that specifies a preheader preceding the metafile header.

### -param deleteWmf [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the Windows handle to a metafile is deleted when the metafile is deleted. <b>TRUE</b> specifies that the <i>hWmf</i> Windows handle is deleted, and <b>FALSE</b> specifies that the <i>hWmf</i> Windows handle is not deleted. The default value is <b>FALSE</b>.

## -remarks

Placeable metafiles are WMF files that contain a preheader preceding the metafile header. The preheader contains additional information for the metafile header of the metafile.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-pwmfrect16">PWMFRect16</a>