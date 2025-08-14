---
UID: NF:winddi.EngUnicodeToMultiByteN
title: EngUnicodeToMultiByteN function (winddi.h)
description: The EngUnicodeToMultiByteN function converts the specified Unicode string into an ANSI string using the current ANSI code page.
helpviewer_keywords: ["EngUnicodeToMultiByteN","EngUnicodeToMultiByteN function [Display Devices]","display.engunicodetomultibyten","gdifncs_4c6f2a59-787b-48a8-9676-c9a88f4201f4.xml","winddi/EngUnicodeToMultiByteN"]
old-location: display\engunicodetomultibyten.htm
tech.root: display
ms.assetid: 5c36322f-7a88-4c24-9f98-aaf3d30f3be4
ms.date: 12/05/2018
ms.keywords: EngUnicodeToMultiByteN, EngUnicodeToMultiByteN function [Display Devices], display.engunicodetomultibyten, gdifncs_4c6f2a59-787b-48a8-9676-c9a88f4201f4.xml, winddi/EngUnicodeToMultiByteN
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
 - EngUnicodeToMultiByteN
 - winddi/EngUnicodeToMultiByteN
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
 - EngUnicodeToMultiByteN
---

# EngUnicodeToMultiByteN function


## -description

The <b>EngUnicodeToMultiByteN</b> function converts the specified Unicode string into an ANSI string using the current ANSI code page.

## -parameters

### -param MultiByteString [out]

Pointer to the buffer that receives the resultant ANSI string.

### -param MaxBytesInMultiByteString [in]

Specifies the maximum number of bytes to be written to <i>MultiByteString. </i>If this value is too small, causing <i>MultiByteString</i> to be a truncated equivalent of <i>UnicodeString</i>, then no error condition results.

### -param BytesInMultiByteString [out, optional]

Pointer to a ULONG that receives the number of bytes written to <i>MultiByteString</i>.

### -param UnicodeString [in]

Pointer to the Unicode source string that is to be converted to ANSI.

### -param BytesInUnicodeString [in]

Specifies the number of bytes in <i>UnicodeString.</i>

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmultibytetounicoden">EngMultiByteToUnicodeN</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwidechartomultibyte">EngWideCharToMultiByte</a>