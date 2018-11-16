---
UID: NF:gdiplusheaders.Metafile.Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL)
title: Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL)
author: windows-sdk-content
description: Creates a Windows GDI+Metafile::Metafile object for recording. The format will be placeable metafile.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_34hwmf_wmfplaceablefileheader_deletewmf.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(HMETAFILE,const WmfPlaceableFileHeader*,BOOL), Metafile.Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL), Metafile::Metafile, Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL), _gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_, gdiplus._gdiplus_CLASS_Metafile_Metafile_hWmf_wmfPlaceableFileHeader_deleteWmf_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - Metafile.Metafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Metafile.Metafile
: 
req.product: GDI+ 1.0
---

# Metafile::Metafile(IN HMETAFILE,IN const WmfPlaceableFileHeader,IN BOOL)


## -description


Creates a Windows GDI+<b>Metafile::Metafile</b> object for recording. The format will be placeable metafile.


## -parameters




### -param hWmf [in]

Type: <b>HMETAFILE</b>

Windows handle to a metafile. 


### -param wmfPlaceableFileHeader [in]

Type: <b>const <a href="https://msdn.microsoft.com/d8315d7d-b613-4175-b7cd-7a36cb411a12">WmfPlaceableFileHeader</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d8315d7d-b613-4175-b7cd-7a36cb411a12">WmfPlaceableFileHeader</a> structure that specifies a preheader preceding the metafile header. 


### -param deleteWmf [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the Windows handle to a metafile is deleted when the metafile is deleted. <b>TRUE</b> specifies that the <i>hWmf</i> Windows handle is deleted, and <b>FALSE</b> specifies that the <i>hWmf</i> Windows handle is not deleted. The default value is <b>FALSE</b>. 


## -remarks



Placeable metafiles are WMF files that contain a preheader preceding the metafile header. The preheader contains additional information for the metafile header of the metafile.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/43c3a37c-0703-4bb5-9091-c33f6a388995">PWMFRect16</a>
 

 

