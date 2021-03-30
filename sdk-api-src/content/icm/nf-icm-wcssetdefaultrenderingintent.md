---
UID: NF:icm.WcsSetDefaultRenderingIntent
title: WcsSetDefaultRenderingIntent
description: Sets the default rendering intent in the specified profile management scope.
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
 - WcsSetDefaultRenderingIntent
f1_keywords:
 - WcsSetDefaultRenderingIntent
 - icm/WcsSetDefaultRenderingIntent
dev_langs:
 - c++
---

## -description

Sets the default rendering intent in the specified profile management scope.

## -parameters

### -param scope

The profile management scope for this operation, which can be system-wide or the current user only.

### -param dwRenderingIntent

The rendering intent. It can be set to one of the following values:

INTENT\_PERCEPTUAL

INTENT\_RELATIVE\_COLORIMETRIC

INTENT\_SATURATION

INTENT\_ABSOLUTE\_COLORIMETRIC

DWORD\_MAX

If *dwRenderingIntent* is DWORD\_MAX and *scope* is WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, the default rendering intent for the current user reverts to the system-wide default.

For more information, see [Rendering intents](/windows/win32/wcs/rendering-intents).

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
