---
UID: NF:icm.CMGetPS2ColorRenderingIntent
title: CMGetPS2ColorRenderingIntent
description: Retrieves the PostScript Level 2 color [rendering intent](/windows/win32/wcs/r) from a profile.
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
req.lib: 
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
 - icm.h
api_name:
 - CMGetPS2ColorRenderingIntent
f1_keywords:
 - CMGetPS2ColorRenderingIntent
 - icm/CMGetPS2ColorRenderingIntent
dev_langs:
 - c++
---

## -description

Retrieves the PostScript Level 2 color rendering intent from a profile.

## -parameters

### -param hProfile

Specifies the profile to use.

### -param dwIntent

Specifies the desired rendering intent to retrieve. Can be one of the following values:

INTENT\_PERCEPTUAL  
INTENT\_SATURATION  
INTENT\_RELATIVE\_COLORIMETRIC  
INTENT\_ABSOLUTE\_COLORIMETRIC

For more information, see [Rendering Intents](/windows/win32/wcs/rendering-intents).

### -param lpBuffer

Points to a buffer in which the color rendering intent is to be placed. If the pointer is NULL, the function returns the size required for this buffer in *\*lpcbSize*.

### -param lpcbSize

Points to a variable specifying the size of the buffer. On return, the variable contains has the number of bytes actually copied to the buffer.

## -returns

If this function succeeds, the return value is TRUE. It also returns TRUE if it is called with *lpBuffer* set to NULL and the size of the required buffer is copied into *lpcbSize*.

If this function fails, the return value is FALSE. When this occurs, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

This function is optional for all CMMs.

If a CMM does not support this function, Windows uses the default CMM to get the color rendering intent.

If the tag is not present in the profile indicated by *hProfile*, the CMM creates it. The resulting rendering intent can be used as the operand for the PostScript Level 2 **findcolorrendering** operator.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
