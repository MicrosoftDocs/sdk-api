---
UID: NF:icm.GetPS2ColorRenderingIntent
title: GetPS2ColorRenderingIntent
description: Retrieves the PostScript Level 2 color [rendering intent](/windows/win32/wcs/r) from an ICC color profile.
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
 - GetPS2ColorRenderingIntent
f1_keywords:
 - GetPS2ColorRenderingIntent
 - icm/GetPS2ColorRenderingIntent
dev_langs:
 - c++
---

## -description

Retrieves the PostScript Level 2 color [rendering intent](/windows/win32/wcs/r) from an ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param dwIntent

Specifies the desired rendering intent to retrieve. Valid values are:

INTENT\_PERCEPTUAL

INTENT\_SATURATION

INTENT\_RELATIVE\_COLORIMETRIC

INTENT\_ABSOLUTE\_COLORIMETRIC

For more information, see [Rendering Intents](/windows/win32/wcs/rendering-intents).

### -param pBuffer

Points to a buffer in which the color rendering intent is to be placed. If the *pBuffer* pointer is set to **NULL**, the buffer size required is returned in *\*pcbSize*.

### -param pcbPS2ColorRenderingIntent

Points to a variable containing the buffer size in bytes. On return, this variable contains the number of bytes actually copied.

## -returns

If this function succeeds, the return value is **TRUE**. If this function succeeds, the return value is **TRUE**. It also returns **TRUE** if the *pBuffer* parameter is **NULL** and the size required for the buffer is copied into *pcbSize.*

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

The rendering intent returned by **GetPS2ColorRenderingIntent** can be used as the operand for the PostScript Level 2 findcolorrendering operator.

This method does not support WCS profiles.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
