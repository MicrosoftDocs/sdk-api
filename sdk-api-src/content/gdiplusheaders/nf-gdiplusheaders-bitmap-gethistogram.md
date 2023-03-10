---
UID: NF:gdiplusheaders.Bitmap.GetHistogram
title: Bitmap::GetHistogram (gdiplusheaders.h)
description: The Bitmap::GetHistogram method returns one or more histograms for specified color channels of this Bitmap object.
helpviewer_keywords: ["Bitmap class [GDI+]","GetHistogram method","Bitmap.GetHistogram","Bitmap::GetHistogram","GetHistogram","GetHistogram method [GDI+]","GetHistogram method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_GetHistogram_","gdiplus._gdiplus_CLASS_Bitmap_GetHistogram_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetHistogram_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapgethistogrammethods\gethistogram.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],GetHistogram method, Bitmap.GetHistogram, Bitmap::GetHistogram, GetHistogram, GetHistogram method [GDI+], GetHistogram method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetHistogram_, gdiplus._gdiplus_CLASS_Bitmap_GetHistogram_
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
 - Bitmap::GetHistogram
 - gdiplusheaders/Bitmap::GetHistogram
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
 - Bitmap.GetHistogram
---

# Bitmap::GetHistogram


## -description

The <b>Bitmap::GetHistogram</b> method returns one or more histograms for specified color channels of this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -parameters

### -param format [in]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-histogramformat">HistogramFormat</a></b>

Element of the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-histogramformat">HistogramFormat</a> enumeration that specifies the channels for which histograms will be created.

### -param NumberOfEntries [in]

Type: <b>UINT</b>

Integer that specifies the number of elements (of type <b>UINT</b>) in each of the arrays pointed to by <i>channel0</i>, <i>channel1</i>, <i>channel2</i>, and <i>channel3</i>. You must allocate memory for those arrays before you call <b>Bitmap::GetHistogram</b>. To determine the required number of elements, call <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethistogramsize">Bitmap::GetHistogramSize</a>.

### -param channel0 [out]

Type: <b>UINT*</b>

Pointer to an array of <b>UINT</b>s that receives the first histogram.

### -param channel1 [out]

Type: <b>UINT*</b>

Pointer to an array of <b>UINT</b>s that receives the second histogram if there is a second histogram. Pass <b>NULL</b> if there is no second histogram.

### -param channel2 [out]

Type: <b>UINT*</b>

Pointer to an array of <b>UINT</b>s that receives the third histogram if there is a third histogram. Pass <b>NULL</b> if there is no third histogram.

### -param channel3 [out]

Type: <b>UINT*</b>

Pointer to an array of <b>UINT</b>s that receives the fourth histogram if there is a fourth histogram. Pass <b>NULL</b> if there is no fourth histogram.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The number of histograms returned depends on the <a href="/windows/desktop/api/gdipluscolormatrix/ne-gdipluscolormatrix-histogramformat">HistogramFormat</a> enumeration element passed to the <i>format</i> parameter. For example, if <i>format</i> is equal to <b>HistogramFormatRGB</b>, then three histograms are returned: one each for the red, green, and blue channels. In that case, <i>channel0</i> points to the array that receives the red-channel histogram, <i>channel1</i> points to the array that receives the green-channel histogram, and <i>channel2</i> points to the array that receives the blue-channel histogram. For <b>HistogramFormatRGB</b>, <i>channel3</i> must be set to <b>NULL</b> because there is no fourth histogram. For more details, see the <b>HistogramFormat</b> enumeration.


#### Examples



The following example constructs a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object from a BMP file. The code retrieves three histograms from the bitmap: one each for the red, green, and blue channels. Note the order of RGB in the name of the enumeration element <b>HistogramFormatRGB</b>. R is first, so it corresponds with <b>ch0</b>. Green is second, so it corresponds with <b>ch1</b>. Blue is third, so it corresponds with <b>ch2</b>. The final parameter passed to <b>Bitmap::GetHistogram</b> is <b>NULL</b> because there is no fourth histogram.


```cpp
Bitmap myBitmap(L"Picture.bmp");

UINT numEntries;
myBitmap.GetHistogramSize(HistogramFormatRGB, &numEntries);

UINT* ch0 = new UINT[numEntries];
UINT* ch1 = new UINT[numEntries];
UINT* ch2 = new UINT[numEntries];

myBitmap.GetHistogram(HistogramFormatRGB, numEntries, ch0, ch1, ch2, NULL);

// Print the histogram values for the three channels: red, green, blue.
for(UINT j = 0; j < numEntries; ++j)
{
   printf("%u\t%u\t%u\t%u\n", j, ch0[j], ch1[j], ch2[j]);
}

delete ch0;
delete ch1;
delete ch2;
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>