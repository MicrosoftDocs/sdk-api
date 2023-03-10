---
UID: NF:icm.GetPS2ColorRenderingDictionary
title: GetPS2ColorRenderingDictionary
description: Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.
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
 - GetPS2ColorRenderingDictionary
f1_keywords:
 - GetPS2ColorRenderingDictionary
 - icm/GetPS2ColorRenderingDictionary
dev_langs:
 - c++
---

## -description

Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param dwIntent

Specifies the desired rendering intent for the color rendering dictionary. Valid values are:

* INTENT\_PERCEPTUAL
* INTENT\_SATURATION
* INTENT\_RELATIVE\_COLORIMETRIC
* INTENT\_ABSOLUTE\_COLORIMETRIC

For more information, see [Rendering intents](/windows/win32/wcs/rendering-intents).

### -param pPS2ColorRenderingDictionary

Pointer to a buffer in which the color rendering dictionary is to be placed. If the *pBuffer* pointer is set to **NULL**, the required buffer size is returned in *\*pcbSize*.

### -param pcbPS2ColorRenderingDictionary

Pointer to a variable containing the size of the buffer in bytes. On return, the variable contains the number of bytes actually copied.

### -param pbBinary

Pointer to a Boolean variable. If **TRUE**, the color rendering dictionary could be copied in binary form. If **FALSE**, the dictionary will be encoded in ASCII85 form. On return, this Boolean variable indicates whether the dictionary was actually binary (**TRUE**) or ASCII85 (**FALSE**).

## -returns

If this function succeeds, the return value is **TRUE**. It also returns **TRUE** if the *pBuffer* parameter is **NULL** and the size required for the buffer is copied into *pcbSize.*

If this function fails, the return value is **FALSE**.

## -remarks

If the dictionary is not available in the profile, the **GetPS2ColorRenderingDictionary** function builds one using the profile contents. This dictionary can then be used as the operand for the PostScript Level 2 **setcolorrendering** operator.

This method does not support WCS profiles.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
