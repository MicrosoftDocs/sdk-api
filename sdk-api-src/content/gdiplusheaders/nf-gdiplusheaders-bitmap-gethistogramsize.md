---
UID: NF:gdiplusheaders.Bitmap.GetHistogramSize
title: Bitmap::GetHistogramSize (gdiplusheaders.h)
description: The Bitmap::GetHistogramSize returns the number of elements (in an array of UINTs) that you must allocate before you call the Bitmap::GetHistogram method of a Bitmap object.
helpviewer_keywords: ["Bitmap class [GDI+]","GetHistogramSize method","Bitmap.GetHistogramSize","Bitmap::GetHistogramSize","GetHistogramSize","GetHistogramSize method [GDI+]","GetHistogramSize method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_GetHistogramSize_","gdiplus._gdiplus_CLASS_Bitmap_GetHistogramSize_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetHistogramSize_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapgethistogrammethods\gethistogramsize.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],GetHistogramSize method, Bitmap.GetHistogramSize, Bitmap::GetHistogramSize, GetHistogramSize, GetHistogramSize method [GDI+], GetHistogramSize method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetHistogramSize_, gdiplus._gdiplus_CLASS_Bitmap_GetHistogramSize_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Bitmap::GetHistogramSize
 - gdiplusheaders/Bitmap::GetHistogramSize
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
 - Bitmap.GetHistogramSize
---

# Bitmap::GetHistogramSize


## -description

The <b>Bitmap::GetHistogramSize</b> returns the number of elements (in an array of <b>UINT</b>s) that you must allocate before you call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method of a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -parameters

### -param format [in]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-histogramformat">HistogramFormat</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-histogramformat">HistogramFormat</a> enumeration that specifies the pixel format of the bitmap.

### -param NumberOfEntries [out]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that receives the number of entries.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>