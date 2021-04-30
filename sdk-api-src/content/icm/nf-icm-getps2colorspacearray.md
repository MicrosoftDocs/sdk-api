---
UID: NF:icm.GetPS2ColorSpaceArray
title: GetPS2ColorSpaceArray
description: Retrieves the PostScript Level 2 [color space](/windows/win32/wcs/c) array from an ICC color profile.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
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
 - mscms.dll
api_name:
 - GetPS2ColorSpaceArray
f1_keywords:
 - GetPS2ColorSpaceArray
 - icm/GetPS2ColorSpaceArray
dev_langs:
 - c++
---

## -description

Retrieves the PostScript Level 2 [color space](/windows/win32/wcs/color-spaces) array from an ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC profile from which to retrieve the PostScript Level 2 color space array.

### -param dwIntent

Specifies the desired rendering intent for the color space array. This field may take one of the following values:

INTENT\_PERCEPTUAL

INTENT\_SATURATION

INTENT\_RELATIVE\_COLORIMETRIC

INTENT\_ABSOLUTE\_COLORIMETRIC

For more information, see [Rendering Intents](/windows/win32/wcs/rendering-intents).

### -param dwCSAType

Specifies the type of color space array. See [Color Space Type Identifiers](/windows/win32/wcs/color-space-type-identifiers).

### -param pPS2ColorSpaceArray

Pointer to a buffer in which the color space array is to be placed. If the *pBuffer* pointer is set to **NULL**, the function returns the required size of the buffer in the memory location pointed to by *pcbSize*.

### -param pcbPS2ColorSpaceArray

Pointer to a variable containing the size of the buffer in bytes. On return, it contains the number of bytes copied into the buffer.

### -param pbBinary

Pointer to a Boolean variable. If set to **TRUE**, the data copied could be binary. If set to **FALSE**, data should be encoded as ASCII85. On return, the memory location pointed to by *pbBinary* indicates whether the data returned actually is binary (**TRUE**) or ASCII85 (**FALSE**).

## -returns

If this function succeeds, the return value is **TRUE**. It also returns **TRUE** if the *pBuffer* parameter is **NULL** and the size required for the buffer is copied into *pcbSize.*

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the color space array is not available in the profile, the **GetPS2ColorSpaceArray** function builds a PostScript Level 2 color space array using the profile contents. This array can then be used as the operand for the PostScript Level2 setcolorspace operator.

This method does not support WCS profiles.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
