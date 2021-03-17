---
UID: NE:gdipluscolormatrix.HistogramFormat
title: HistogramFormat (gdipluscolormatrix.h)
description: The HistogramFormat enumeration specifies the number and type of histograms that represent the color channels of a bitmap. This enumeration is used with the Bitmap::GetHistogram method.
helpviewer_keywords: ["HistogramFormat","HistogramFormat enumeration [GDI+]","HistogramFormatA","HistogramFormatARGB","HistogramFormatB","HistogramFormatG","HistogramFormatGray","HistogramFormatPARGB","HistogramFormatR","HistogramFormatRGB","_gdiplus_ENUM_HistogramFormat","gdiplus._gdiplus_ENUM_HistogramFormat","gdipluscolormatrix/HistogramFormat","gdipluscolormatrix/HistogramFormatA","gdipluscolormatrix/HistogramFormatARGB","gdipluscolormatrix/HistogramFormatB","gdipluscolormatrix/HistogramFormatG","gdipluscolormatrix/HistogramFormatGray","gdipluscolormatrix/HistogramFormatPARGB","gdipluscolormatrix/HistogramFormatR","gdipluscolormatrix/HistogramFormatRGB"]
old-location: gdiplus\_gdiplus_ENUM_HistogramFormat.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\histogramformat.htm
ms.date: 12/05/2018
ms.keywords: HistogramFormat, HistogramFormat enumeration [GDI+], HistogramFormatA, HistogramFormatARGB, HistogramFormatB, HistogramFormatG, HistogramFormatGray, HistogramFormatPARGB, HistogramFormatR, HistogramFormatRGB, _gdiplus_ENUM_HistogramFormat, gdiplus._gdiplus_ENUM_HistogramFormat, gdipluscolormatrix/HistogramFormat, gdipluscolormatrix/HistogramFormatA, gdipluscolormatrix/HistogramFormatARGB, gdipluscolormatrix/HistogramFormatB, gdipluscolormatrix/HistogramFormatG, gdipluscolormatrix/HistogramFormatGray, gdipluscolormatrix/HistogramFormatPARGB, gdipluscolormatrix/HistogramFormatR, gdipluscolormatrix/HistogramFormatRGB
req.header: gdipluscolormatrix.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - HistogramFormat
 - gdipluscolormatrix/HistogramFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GdiplusColorMatrix.h
api_name:
 - HistogramFormat
---

# HistogramFormat enumeration


## -description

The <b>HistogramFormat</b> enumeration specifies the number and type of histograms that represent the color channels of a bitmap. This enumeration is used with the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method.

## -enum-fields

### -field HistogramFormatARGB

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns four histograms: one each for the alpha, red, green, and blue channels. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The red-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The green-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The blue-channel histogram is written to the buffer pointed to by the <i>channel3</i> parameter.

### -field HistogramFormatPARGB

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns four histograms: one each for the alpha, red, green, and blue channels. The red, green, and blue channels are each multiplied by the alpha channel before the histograms are created. The bitmap is not permanently altered when the color channels are multiplied by the alpha channel; that multiplication is only for the purpose of creating the histograms. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The red-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The green-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The blue-channel histogram is written to the buffer pointed to by the <i>channel3</i> parameter.

### -field HistogramFormatRGB

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns three histograms: one each for the red, green, and blue channels. The red-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The green-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The blue-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The <i>channel3</i> parameter must be set to <b>NULL</b>.

### -field HistogramFormatGray

Specifies that each pixel is converted to a grayscale value in the range 0 through 255, and then one histogram, based on those grayscale value, is returned. The bitmap is not permanently altered by the conversion to grayscale values; those values are calculated only for the purpose of creating the histogram. The grayscale histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.

### -field HistogramFormatB

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns a histogram for the blue channel. The blue-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.

### -field HistogramFormatG

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns a histogram for the green channel. The green-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.

### -field HistogramFormatR

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns a histogram for the red channel. The red-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.

### -field HistogramFormatA

Specifies that the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogram">Bitmap::GetHistogram</a> method returns a histogram for the alpha channel. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.