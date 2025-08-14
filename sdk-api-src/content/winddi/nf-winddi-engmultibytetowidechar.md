---
UID: NF:winddi.EngMultiByteToWideChar
title: EngMultiByteToWideChar function (winddi.h)
description: The EngMultiByteToWideChar function converts an ANSI source string into a wide character string using the specified code page.
helpviewer_keywords: ["EngMultiByteToWideChar","EngMultiByteToWideChar function [Display Devices]","display.engmultibytetowidechar","gdifncs_217d1045-3661-401b-af6e-148668ed97e4.xml","winddi/EngMultiByteToWideChar"]
old-location: display\engmultibytetowidechar.htm
tech.root: display
ms.assetid: 7ed4f718-e28d-40d9-a3e0-c6961281a319
ms.date: 12/05/2018
ms.keywords: EngMultiByteToWideChar, EngMultiByteToWideChar function [Display Devices], display.engmultibytetowidechar, gdifncs_217d1045-3661-401b-af6e-148668ed97e4.xml, winddi/EngMultiByteToWideChar
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngMultiByteToWideChar
 - winddi/EngMultiByteToWideChar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngMultiByteToWideChar
---

# EngMultiByteToWideChar function


## -description

The <b>EngMultiByteToWideChar</b> function converts an ANSI source string into a wide character string using the specified code page.

## -parameters

### -param CodePage [in]

Specifies the code page to use to perform the translation.

### -param WideCharString [out, optional]

Pointer to the buffer into which the translated character string is copied.

### -param BytesInWideCharString [in]

Specifies the size, in bytes, of <i>WideCharString</i>. If <i>WideCharString</i> is not large enough to contain the translation, <b>EngMultiByteToWideChar</b> truncates the string, and does not report an error.

### -param MultiByteString [in, optional]

Pointer to the buffer containing the multibyte string to be translated.

### -param BytesInMultiByteString [in]

Specifies the number of bytes in <i>MultiByteString.</i>

## -returns

The <b>EngMultiByteToWideChar</b> function returns the number of bytes it converted to wide character form, if successful. Otherwise, the function returns -1.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engunicodetomultibyten">EngUnicodeToMultiByteN</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwidechartomultibyte">EngWideCharToMultiByte</a>