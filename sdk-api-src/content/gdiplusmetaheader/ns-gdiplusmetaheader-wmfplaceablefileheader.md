---
UID: NS:gdiplusmetaheader.WmfPlaceableFileHeader
title: WmfPlaceableFileHeader (gdiplusmetaheader.h)
description: The WmfPlaceableFileHeader structure defines the fields of a placeable metafile header. Placeable metafiles were created as a way of specifying how a metafile is mapped and scaled on a display device.
helpviewer_keywords: ["WmfPlaceableFileHeader","WmfPlaceableFileHeader structure [GDI+]","_gdiplus_STRUC_WmfPlaceableFileHeader","gdiplus._gdiplus_STRUC_WmfPlaceableFileHeader","gdiplusmetaheader/WmfPlaceableFileHeader"]
old-location: gdiplus\_gdiplus_STRUC_WmfPlaceableFileHeader.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\wmfplaceablefileheader.htm
ms.date: 12/05/2018
ms.keywords: WmfPlaceableFileHeader, WmfPlaceableFileHeader structure [GDI+], _gdiplus_STRUC_WmfPlaceableFileHeader, gdiplus._gdiplus_STRUC_WmfPlaceableFileHeader, gdiplusmetaheader/WmfPlaceableFileHeader
req.header: gdiplusmetaheader.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WmfPlaceableFileHeader
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - WmfPlaceableFileHeader
 - gdiplusmetaheader/WmfPlaceableFileHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusmetaheader.h
api_name:
 - WmfPlaceableFileHeader
---

# WmfPlaceableFileHeader structure


## -description

The <b>WmfPlaceableFileHeader</b> structure defines the fields of a placeable metafile header. Placeable metafiles were created as a way of specifying how a metafile is mapped and scaled on a display device.

## -struct-fields

### -field Key

Type: <b>UINT32</b>

Identification value that indicates the presence of a placeable metafile header. This value is always 0x9AC6CDD7.

### -field Hmf

Type: <b>INT16</b>

Handle to the metafile in memory. When written to disk, this field is not used and will always contains the value 0.

### -field BoundingBox

Type: <b><a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-pwmfrect16">PWMFRect16</a></b>

Destination rectangle, measured in twips, for displaying the metafile.

### -field Inch

Type: <b>INT16</b>

Number of twips per inch used to represent the image.

Normally, there are 1440 twips per inch; however, this number can be changed to scale the image. 
						<ul>
<li>A value of 720 specifies that the image is twice its normal size. </li>
<li>A value of 360 specifies that the image is four times its normal size. </li>
<li>A value of 2880 specifies that the image is half its normal size. </li>
</ul>

### -field Reserved

Type: <b>UINT32</b>

Not used and is always set to 0.

### -field Checksum

Type: <b>INT16</b>

Checksum for the previous 10 <b>WORD</b><b>s</b> in the header. This value can be used to determine whether the metafile has become corrupted.

## -remarks

Although placeable metafiles are quite common, they are not directly supported by the Windows API. To display a placeable metafile using the Windows API, you must first strip the placeable metafile header from the file. This is typically performed by copying the metafile to a temporary file starting at file offset 22 (0x16). This is because each placeable metafile begins with a 22-byte header that is followed by a standard metafile.

## -see-also

<a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-pwmfrect16">PWMFRect16</a>

