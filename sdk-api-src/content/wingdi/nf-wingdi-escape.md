---
UID: NF:wingdi.Escape
title: Escape function (wingdi.h)
description: Enables an application to access the system-defined device capabilities that are not available through GDI.
helpviewer_keywords: ["Escape","Escape function [Windows GDI]","_win32_Escape_v3","gdi.escape","wingdi/Escape"]
old-location: gdi\escape.htm
tech.root: xps
ms.assetid: ba21b680-78a8-45a2-94e1-01b377b74787
ms.date: 12/05/2018
ms.keywords: Escape, Escape function [Windows GDI], _win32_Escape_v3, gdi.escape, wingdi/Escape
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Escape
 - wingdi/Escape
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
 - Escape
---

# Escape function


## -description

The <b>Escape</b> function enables an application to access the system-defined device capabilities that are not available through GDI. Escape calls made by an application are translated and sent to the driver.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iEscape [in]

The escape function to be performed. This parameter must be one of the predefined escape values listed in Remarks. Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-extescape">ExtEscape</a> function if your application defines a private escape value.

### -param cjIn [in]

The number of bytes of data pointed to by the <i>lpvInData</i> parameter. This can be 0.

### -param pvIn [in]

A pointer to the input structure required for the specified escape.

### -param pvOut [out]

A pointer to the structure that receives output from this escape. This parameter should be <b>NULL</b> if no data is returned.

## -returns

If the function succeeds, the return value is greater than zero, except with the <a href="/previous-versions/windows/desktop/legacy/ff686811(v=vs.85)">QUERYESCSUPPORT</a> printer escape, which checks for implementation only. If the escape is not implemented, the return value is zero.

If the function fails, the return value is a system error code.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The effect of passing 0 for <i>cbInput</i> will depend on the value of <i>nEscape</i> and on the driver that is handling the escape.

Of the original printer escapes, only the following can be used.

<table>
<tr>
<th>Escape</th>
<th>Description</th>
</tr>
<tr>
<td>
QUERYESCSUPPORT

</td>
<td>
Determines whether a particular escape is implemented by the device driver.

</td>
</tr>
<tr>
<td>
PASSTHROUGH

</td>
<td>
Allows the application to send data directly to a printer.

</td>
</tr>
</table>
 

For information about printer escapes, see <a href="/windows/desktop/api/wingdi/nf-wingdi-extescape">ExtEscape</a>.

Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a> function to prepare the printer driver to receive data.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-abortdoc">AbortDoc</a>



<a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enddoc">EndDoc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-endpage">EndPage</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extescape">ExtEscape</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printerproperties">PrinterProperties</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setabortproc">SetAbortProc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startdoca">StartDoc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startpage">StartPage</a>