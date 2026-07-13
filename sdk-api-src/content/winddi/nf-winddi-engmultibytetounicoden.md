---
UID: NF:winddi.EngMultiByteToUnicodeN
title: EngMultiByteToUnicodeN function (winddi.h)
description: The EngMultiByteToUnicodeN function converts the specified ANSI source string into a Unicode string using the current ANSI code page.
helpviewer_keywords: ["EngMultiByteToUnicodeN","EngMultiByteToUnicodeN function [Display Devices]","display.engmultibytetounicoden","gdifncs_ad2cf58d-ac6c-438f-b9be-74e2617a857c.xml","winddi/EngMultiByteToUnicodeN"]
old-location: display\engmultibytetounicoden.htm
tech.root: display
ms.assetid: fa7a4e64-46be-49c8-9862-04348b9dc79e
ms.date: 12/05/2018
ms.keywords: EngMultiByteToUnicodeN, EngMultiByteToUnicodeN function [Display Devices], display.engmultibytetounicoden, gdifncs_ad2cf58d-ac6c-438f-b9be-74e2617a857c.xml, winddi/EngMultiByteToUnicodeN
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
 - EngMultiByteToUnicodeN
 - winddi/EngMultiByteToUnicodeN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngMultiByteToUnicodeN
---

# EngMultiByteToUnicodeN function


## -description

The <b>EngMultiByteToUnicodeN</b> function converts the specified ANSI source string into a Unicode string using the current ANSI code page.

## -parameters

### -param UnicodeString [out]

Pointer to the buffer that receives the resultant Unicode string.

### -param MaxBytesInUnicodeString [in]

Supplies the maximum number of bytes to be written to <i>UnicodeString. </i>If this value is too small, causing <i>UnicodeString</i> to be a truncated equivalent of <i>MultiByteString</i>, no error condition results.

### -param BytesInUnicodeString [out, optional]

Pointer to a ULONG that receives the number of bytes written to <i>UnicodeString</i>.

### -param MultiByteString [in]

Pointer to the ANSI source string that is to be converted to Unicode.

### -param BytesInMultiByteString [in]

Specifies the number of bytes in <i>MultiByteString.</i>

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmultibytetowidechar">EngMultiByteToWideChar</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunicodetomultibyten">EngUnicodeToMultiByteN</a>