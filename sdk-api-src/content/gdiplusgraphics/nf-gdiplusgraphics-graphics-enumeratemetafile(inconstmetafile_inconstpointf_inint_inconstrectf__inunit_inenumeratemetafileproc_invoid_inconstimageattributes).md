---
UID: NF:gdiplusgraphics.Graphics.EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)
title: Graphics::EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::EnumerateMetafile method calls an application-defined callback function for each record in a specified metafile. You can use this method to display a metafile by calling PlayRecord in the callback function.
old-location: gdiplus\_gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoints_INT_count_RectF_srcRec.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsenumeratemetafilemethods\enumeratemetafile_91metafilemetafile_pointfdestpoints_intc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateMetafile, EnumerateMetafile method [GDI+], EnumerateMetafile method [GDI+],Graphics class, Graphics class [GDI+],EnumerateMetafile method, Graphics.EnumerateMetafile, Graphics.EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes), Graphics.EnumerateMetafile(const Metafile*,const Point*,INT,const RectF&,Unit,EnumerateMetafileProc,VOID*,ImageAttributes*), Graphics::EnumerateMetafile, Graphics::EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes), _gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoints_INT_count_RectF_srcRec, gdiplus._gdiplus_CLASS_Graphics_EnumerateMetafile_Metafile_metafile_PointF_destPoints_INT_count_RectF_srcRec
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.EnumerateMetafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::EnumerateMetafile(IN const Metafile,IN const PointF,IN INT,IN const RectF &,IN Unit,IN EnumerateMetafileProc,IN VOID,IN const ImageAttributes)


## -description


The <b>Graphics::EnumerateMetafile</b> method calls an application-defined callback function for each record in a specified metafile. You can use this method to display a metafile by calling 
			<a href="https://msdn.microsoft.com/en-us/library/ms535274(v=VS.85).aspx">PlayRecord</a> in the callback function.


## -parameters




### -param metafile [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>*</b>

Pointer to a metafile to be enumerated. 


### -param destPoints [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to an array of destination points. This is an array of three points that defines the destination parallelogram for the displayed metafile. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>destPoints</i> array. 


### -param srcRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to the rectangle that specifies the portion of the metafile that is displayed. 


### -param srcUnit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a> enumeration that specifies the unit of measure for the source rectangle. 


### -param callback [in]

Type: <b>EnumerateMetafileProc</b>

Pointer to an application-defined callback function. The prototype for the callback function is given in Gdiplustypes.h. 


### -param callbackData [in]

Type: <b>VOID*</b>

Optional. Pointer to a block of data that is passed to the callback function. The default value is <b>NULL</b>. 


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>*</b>

Optional. Pointer to an 
					<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object that specifies color adjustments for the displayed metafile. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.



