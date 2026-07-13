---
UID: NF:icm.CMTranslateRGBs
title: CMTranslateRGBs
description: Translates a bitmap from one [color space](https://msdn.microsoft.com/en-us/library/dd371818\(v=vs.85\)) to another using a color transform.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icm32.dll
api_name:
 - CMTranslateRGBs
f1_keywords:
 - CMTranslateRGBs
 - icm/CMTranslateRGBs
dev_langs:
 - c++
---

## -description

\[**CMTranslateRGBs** is no longer available for use as of Windows Vista.\]

Translates a bitmap from one [color space](/windows/win32/wcs/c#color-space) to another using a color transform.

## -parameters

### -param hcmTransform

Specifies the color transform to use.

### -param lpSrcBits

Points to the bitmap to translate.

### -param bmInput

Specifies the input bitmap format.

### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.

### -param dwHeight

Specifies the number of scan lines in the input bitmap.

### -param dwStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If *dwStride* is set to zero, the CMM should assume that scan lines are padded so as to be **DWORD**-aligned.

### -param lpDestBits

Points to a destination buffer in which to place the translated bitmap.

### -param bmOutput

Specifies the output bitmap format.

### -param dwTranslateDirection

Specifies the direction of the transform being used for the translation. This parameter must take one of the following values.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="CMS_FORWARD"></span><span id="cms_forward"></span>
<strong>CMS_FORWARD</strong></td>
<td><p>Use forward transform</p></td>
</tr>
<tr class="even">
<td><span id="CMS_BACKWARD"></span><span id="cms_backward"></span>
<strong>CMS_BACKWARD</strong></td>
<td><p>Use reverse transform</p></td>
</tr>
</tbody>
</table>

## -returns

Beginning with Windows Vista, the default CMM (Icm32.dll) will return **FALSE** and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) will report ERROR\_NOT\_SUPPORTED.

**Windows Server 2003, Windows XP and Windows 2000:**

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. If the function is not successful, the CMM should call [SetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) to set the last error to a valid error value defined in Winerror.h.

## -remarks

Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

**Windows Server 2003, Windows XP and Windows 2000:**

Every CMM is required to export this function.

When writing into the destination buffer, the CMM should make sure that scan lines are padded to be **DWORD**-aligned.

If the input and output formats are not compatible with the color transform, this function fails.

If both input and output bitmap formats are 3-channel, 4 bytes-per-pixel as in the case of BM\_xRGBQUADS, the 4th byte should be preserved and copied to the output buffer.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
