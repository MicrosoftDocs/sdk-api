---
UID: NF:winddi.EngSetPrinterData
title: EngSetPrinterData function (winddi.h)
description: The EngSetPrinterData function is obsolete in Windows 2000 and later. In earlier versions of Windows EngSetPrinterData sets the configuration data for the specified printer.
helpviewer_keywords: ["EngSetPrinterData","EngSetPrinterData function [Display Devices]","display.engsetprinterdata","gdifncs_5d3c9c7e-f688-4361-8aee-545c7244921a.xml","winddi/EngSetPrinterData"]
old-location: display\engsetprinterdata.htm
tech.root: display
ms.assetid: 8e6ff116-8735-49b1-a67c-70f5d65efb0f
ms.date: 12/05/2018
ms.keywords: EngSetPrinterData, EngSetPrinterData function [Display Devices], display.engsetprinterdata, gdifncs_5d3c9c7e-f688-4361-8aee-545c7244921a.xml, winddi/EngSetPrinterData
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
 - EngSetPrinterData
 - winddi/EngSetPrinterData
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
 - EngSetPrinterData
---

# EngSetPrinterData function


## -description

The <b>EngSetPrinterData</b> function is obsolete in Windows 2000 and later. 

In earlier versions of Windows <b>EngSetPrinterData </b> sets the configuration data for the specified printer.

## -parameters

### -param hPrinter [in]

Handle to the printer for which configuration data should be set. This is the handle that is passed as the <i>hDriver</i> parameter of <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>. See <b>Remarks</b>.

### -param pType [in]

Pointer to a null-terminated string that identifies the data to be set.

### -param dwType [in]

Is a flag that specifies the type of information to be set. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
REG_BINARY

</td>
<td>
Binary data in any form.

</td>
</tr>
<tr>
<td>
REG_DWORD

</td>
<td>
A 32-bit number.

</td>
</tr>
<tr>
<td>
REG_DWORD_BIG_ENDIAN

</td>
<td>
A 32-bit number in big-endian format, meaning that the most significant byte of a word is the low-order byte.

</td>
</tr>
<tr>
<td>
REG_DWORD_LITTLE_ENDIAN

</td>
<td>
A 32-bit number in little-endian format (same as REG_DWORD), meaning that the most significant byte of a word is the high-order byte

</td>
</tr>
<tr>
<td>
REG_EXPAND_SZ

</td>
<td>
A null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%"). It will be a Unicode or ANSI string depending on whether Unicode or ANSI functions are used.

</td>
</tr>
<tr>
<td>
REG_LINK

</td>
<td>
A Unicode symbolic link.

</td>
</tr>
<tr>
<td>
REG_MULTI_SZ

</td>
<td>
An array of null-terminated strings, terminated by two null characters.

</td>
</tr>
<tr>
<td>
REG_NONE

</td>
<td>
No defined value type.

</td>
</tr>
<tr>
<td>
REG_RESOURCE_LIST

</td>
<td>
A device-driver resource list.

</td>
</tr>
<tr>
<td>
REG_SZ

</td>
<td>
A null-terminated string. It will be a Unicode or ANSI string depending on whether you use the Unicode or ANSI functions.

</td>
</tr>
</table>

### -param lpbPrinterData [in]

Pointer to the printer configuration data that is to be set. The type of data pointed to is determined by <i>dwType</i>.

### -param cjPrinterData [in]

Specifies the size, in bytes, of <i>lpbPrinterData</i>.

## -returns

<b>EngSetPrinterData</b> returns the last logged error message.

## -remarks

Beginning with Microsoft Windows 2000, this function is obsolete. The handles used in calls to the <b>EngSetPrinterData</b> and <i>DrvEnablePDEV</i> functions have different access rights; hence these functions no longer work together. The <i>hDriver</i> parameter used in calls to the <i>DrvEnablePDEV</i> function is opened with the PRINTER_ACCESS_USE access right. In contrast, the <i>hPrinter</i> parameter used in calls to the <b>EngSetPrinterData</b> function must have been opened with the PRINTER_ALL_ACCESS access right. As a result, there is no way for a kernel-mode printer driver (the only type of printer driver that can call <b>EngSetPrinterData</b>) to use <b>EngSetPrinterData</b> to write information about a printer to the registry. 

For more information about printer access rights, see the PRINTER_DEFAULTS structure (described in the Windows SDK documentation).

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-enggetprinterdata">EngGetPrinterData</a>