---
UID: NF:gdiplusheaders.Metafile.Metafile(INconstWCHAR,INHDC,INconstRect&,INMetafileFrameUnit,INEmfType,INconstWCHAR)
title: Metafile::Metafile(IN const WCHAR,IN HDC,IN const Rect &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR) (gdiplusheaders.h)
description: Creates a Metafile::Metafile object for recording.
helpviewer_keywords: ["Metafile","Metafile class [GDI+]","Metafile constructor","Metafile constructor [GDI+]","Metafile constructor [GDI+]","Metafile class","Metafile.Metafile","Metafile.Metafile(IN const WCHAR","IN HDC","IN const Rect &","IN MetafileFrameUnit","IN EmfType","IN const WCHAR)","Metafile.Metafile(const WCHAR*","HDC","const Rect&","MetaFileFrameUnit","EmfType","const WCHAR*)","Metafile::Metafile","Metafile::Metafile(IN const WCHAR","IN HDC","IN const Rect &","IN MetafileFrameUnit","IN EmfType","IN const WCHAR)","_gdiplus_CLASS_Metafile_Metafile_WCHAR_fileName_HDC_referenceHdc_Rect_frameRect_MetafileFrameUnit_fr","gdiplus._gdiplus_CLASS_Metafile_Metafile_WCHAR_fileName_HDC_referenceHdc_Rect_frameRect_MetafileFrameUnit_fr"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_WCHAR_fileName_HDC_referenceHdc_Rect_frameRect_MetafileFrameUnit_fr.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_42wcharfilename_hdcreferencehdc_rectampf.htm
ms.date: 12/05/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(IN const WCHAR,IN HDC,IN const Rect &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), Metafile.Metafile(const WCHAR*,HDC,const Rect&,MetaFileFrameUnit,EmfType,const WCHAR*), Metafile::Metafile, Metafile::Metafile(IN const WCHAR,IN HDC,IN const Rect &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), _gdiplus_CLASS_Metafile_Metafile_WCHAR_fileName_HDC_referenceHdc_Rect_frameRect_MetafileFrameUnit_fr, gdiplus._gdiplus_CLASS_Metafile_Metafile_WCHAR_fileName_HDC_referenceHdc_Rect_frameRect_MetafileFrameUnit_fr
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

# Metafile::Metafile(IN const WCHAR,IN HDC,IN const Rect &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)


## -description

Creates a <b>Metafile::Metafile</b> object for recording.

## -parameters

### -param fileName [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of the file in which the metafile will be saved.

### -param referenceHdc [in]

Type: <b>HDC</b>

Handle to a device context that contains attributes of a display device.

### -param frameRect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that bounds the metafile display.

### -param frameUnit [in]

Type: <b>MetaFileFrameUnit</b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-metafileframeunit">MetafileFrameUnit</a> enumeration that specifies the unit of measure for <i>frameRect</i>. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-metafileframeunit">MetafileFrameUnitGdi</a>.

### -param type [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a> enumeration that specifies the type of metafile that will be recorded. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-metafileframeunit">EmfTypeEmfPlusDual</a>.

### -param description [in]

Type: <b>const WCHAR*</b>

Optional. Pointer to a wide-character string that specifies the descriptive name of the metafile. The default value is <b>NULL</b>.

## -remarks

When recording to a file, the file must be writable, and Windows GDI+ must be able to obtain an exclusive lock on the file.

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-metafileframeunit">MetafileFrameUnit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-recording-metafiles-use">Recording Metafiles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>