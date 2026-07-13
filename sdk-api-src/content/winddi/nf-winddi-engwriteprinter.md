---
UID: NF:winddi.EngWritePrinter
title: EngWritePrinter function (winddi.h)
description: The EngWritePrinter function allows printer graphics DLLs to send a data stream to printer hardware.
helpviewer_keywords: ["EngWritePrinter","EngWritePrinter function [Display Devices]","display.engwriteprinter","gdifncs_ec307778-86e1-4f8c-96c8-66c86e196a67.xml","winddi/EngWritePrinter"]
old-location: display\engwriteprinter.htm
tech.root: display
ms.assetid: c65f09b2-5924-479a-8067-a1ba472348e2
ms.date: 12/05/2018
ms.keywords: EngWritePrinter, EngWritePrinter function [Display Devices], display.engwriteprinter, gdifncs_ec307778-86e1-4f8c-96c8-66c86e196a67.xml, winddi/EngWritePrinter
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
 - EngWritePrinter
 - winddi/EngWritePrinter
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
api_name:
 - EngWritePrinter
---

# EngWritePrinter function


## -description

The <b>EngWritePrinter</b> function allows printer graphics DLLs to send a data stream to printer hardware.

## -parameters

### -param hPrinter [in]

Caller-supplied handle to the printer. This should be the handle received as the <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> function's <i>hDriver</i> parameter value.

### -param pBuf [in]

Caller-supplied pointer to a buffer containing a byte stream to be sent to the printer.

### -param cbBuf [in]

Specifies the caller-supplied number of bytes contained in the buffer pointed to by <i>pBuf</i>.

### -param pcWritten [out]

Caller-supplied pointer to a DWORD location that receives the number of bytes actually written to the printer.

## -returns

If the operation succeeds, the function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

<a href="/windows-hardware/drivers/print/printer-graphics-dll">Printer graphics DLLs</a> call <b>EngWritePrinter</b> to send data streams (either control sequences or image data) to the print spooler, which in turn sends the data to the printer hardware by calling the appropriate <a href="/windows-hardware/drivers/">print monitor</a>. The function returns after the spooler receives the data.

The buffer pointed to by <i>pBuf</i> cannot be in user memory; that is, <i>pBuf</i> cannot point to memory allocated by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a> with the BMF_USERMEM flag set or by <a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>.

For additional information about calling <b>EngWritePrinter</b>, see <a href="/windows-hardware/drivers/print/rendering-a-print-job">Rendering a Print Job</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engallocusermem">EngAllocUserMem</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>