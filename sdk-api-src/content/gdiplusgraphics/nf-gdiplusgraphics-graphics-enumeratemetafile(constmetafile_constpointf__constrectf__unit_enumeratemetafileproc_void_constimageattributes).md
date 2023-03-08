---
UID: NF:gdiplusgraphics.Graphics.EnumerateMetafile(constMetafile,constPointF&,constRectF&,Unit,EnumerateMetafileProc,VOID,constImageAttributes)
title: Graphics::EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes) (gdiplusgraphics.h)
description: The Graphics::EnumerateMetafile method calls an application-defined callback function for each record in a specified metafile. You can use this method to display a metafile by calling PlayRecord in the callback function. (overload 1/12)
helpviewer_keywords: ["EnumerateMetafile","EnumerateMetafile method [GDI+]","EnumerateMetafile method [GDI+]","Graphics class","Graphics class [GDI+]","EnumerateMetafile method","Graphics.EnumerateMetafile","Graphics.EnumerateMetafile(IN const Metafile","IN const PointF &","IN const RectF &","IN Unit","IN EnumerateMetafileProc","IN VOID","IN const ImageAttributes)","Graphics.EnumerateMetafile(const Metafile*","const Point&","const Rect&","Unit","EnumerateMetafileProc","VOID*","ImageAttributes*)","Graphics::EnumerateMetafile","Graphics::EnumerateMetafile(IN const Metafile","IN const PointF &","IN const RectF &","IN Unit","IN EnumerateMetafileProc","IN VOID","IN const ImageAttributes)","Graphics::EnumerateMetafile","Graphics::EnumerateMetafile(IN const Metafile","IN const PointF &","IN const RectF &","IN Unit","IN EnumerateMetafileProc","IN VOID","IN const ImageAttributes)","_gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoint_RectF_srcRect_Unit_srcU","gdiplus._gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoint_RectF_srcRect_Unit_srcU"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoint_RectF_srcRect_Unit_srcU.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsenumeratemetafilemethods\enumeratemetafile_76metafilemetafile_pointfampdestpoint_re.htm
ms.date: 12/05/2018
ms.keywords: EnumerateMetafile, EnumerateMetafile method [GDI+], EnumerateMetafile method [GDI+],Graphics class, Graphics class [GDI+],EnumerateMetafile method, Graphics.EnumerateMetafile, Graphics.EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes), Graphics.EnumerateMetafile(const Metafile*,const Point&,const Rect&,Unit,EnumerateMetafileProc,VOID*,ImageAttributes*), Graphics::EnumerateMetafile, Graphics::EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes), Graphics::EnumerateMetafile,Graphics::EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes), _gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoint_RectF_srcRect_Unit_srcU, gdiplus._gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoint_RectF_srcRect_Unit_srcU
req.header: gdiplusgraphics.h
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
 - Graphics::EnumerateMetafile
 - gdiplusgraphics/Graphics::EnumerateMetafile
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
 - Graphics.EnumerateMetafile
---

# Graphics::EnumerateMetafile(IN const Metafile,IN const PointF &,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)


## -description

The <b>Graphics::EnumerateMetafile</b> method calls an application-defined callback function for each record in a specified metafile. You can use this method to display a metafile by calling 
			<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-playrecord">PlayRecord</a> in the callback function.

## -parameters

### -param metafile [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>*</b>

Pointer to a metafile to be enumerated.

### -param destPoint [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point that specifies the upper-left corner of the displayed metafile.

### -param srcRect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that specifies the portion of the metafile that is displayed.

### -param srcUnit [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for the source rectangle.

### -param callback [in]

Type: <b>EnumerateMetafileProc</b>

Pointer to an application-defined callback function. The prototype for the callback function is given in Gdiplustypes.h.

### -param callbackData [in]

Type: <b>VOID*</b>

Optional. Pointer to a block of data that is passed to the callback function. The default value is <b>NULL</b>.

### -param imageAttributes [in]

Type: <b><a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>*</b>

Optional. Pointer to an 
					<a href="/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object that specifies color adjustments for the displayed metafile. The default value is <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.
