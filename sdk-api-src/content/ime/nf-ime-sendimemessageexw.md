---
UID: NF:ime.SendIMEMessageExW
title: SendIMEMessageExW function (ime.h)
description: Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction. (Unicode)
helpviewer_keywords: ["SendIMEMessageEx", "SendIMEMessageEx function [Windows API]", "SendIMEMessageExW", "_win32_SendIMEMessageEx", "ime/SendIMEMessageEx", "ime/SendIMEMessageExW", "winprog._win32_sendimemessageex", "winui._win32_sendimemessageex"]
old-location: winprog\_win32_sendimemessageex.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\sendimemessageex.htm
ms.date: 12/05/2018
ms.keywords: SendIMEMessageEx, SendIMEMessageEx function [Windows API], SendIMEMessageExA, SendIMEMessageExW, _win32_SendIMEMessageEx, ime/SendIMEMessageEx, ime/SendIMEMessageExA, ime/SendIMEMessageExW, winprog._win32_sendimemessageex, winui._win32_sendimemessageex
req.header: ime.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SendIMEMessageExW (Unicode) and SendIMEMessageExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendIMEMessageExW
 - ime/SendIMEMessageExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SendIMEMessageEx
 - SendIMEMessageExA
 - SendIMEMessageExW
---

# SendIMEMessageExW function


## -description

<p class="CCE_Message">[This function is obsolete and should not be used.]

Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.

## -parameters

### -param HWND [in]

The window handle of the application that initiates the transaction. Generally, it is the window that has focus.

### -param LPARAM [in]

A <b>DWORD</b> value in which the low-order word specifies a handle to the global memory that contains an <a href="/windows/desktop/api/ime/ns-ime-imestruct">IMESTRUCT</a> structure. The global memory is allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function. The high-order word is reserved; it is not used.

## -returns

The result of processing of the subfunction. If the result is not success, one of the following error codes is stored into the <b>wParam</b> of the <a href="/windows/desktop/api/ime/ns-ime-imestruct">IMESTRUCT</a> structure.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_DISKERROR</b></dt>
</dl>
</td>
<td width="60%">
Disk error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_ERROR</b></dt>
</dl>
</td>
<td width="60%">
General error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_ILLEGAL</b></dt>
</dl>
</td>
<td width="60%">
Contains an illegal character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Invalid subfunction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_NEST</b></dt>
</dl>
</td>
<td width="60%">
Subfunction is nested and, therefore, cannot be used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_NOIME</b></dt>
</dl>
</td>
<td width="60%">
The IME has not been selected (has not been installed).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_NOROOM</b></dt>
</dl>
</td>
<td width="60%">
Short of area.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No candidate found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_SYSTEMMODAL</b></dt>
</dl>
</td>
<td width="60%">
Windows is in system mode, data cannot be passed to the IME.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IME_RS_TOOLONG</b></dt>
</dl>
</td>
<td width="60%">
Characters too long.

</td>
</tr>
</table>

## -remarks

<b>SendIMEMessageEx</b> guarantees the action stipulated in the specifications only for IMEs that support the <b>WM_CONVERTREQUESTEX</b> message. For an IME that does not support <b>WM_CONVERTREQUESTEX</b>, <b>SendIMEMessageEx</b> sends a <b>WM_CONVERTREQUEST</b> message to the IME and returns the contents of the <b>wParam</b> member of the <a href="/windows/desktop/api/ime/ns-ime-imestruct">IMESTRUCT</a> structure. If the processing of the subfunction has not been completed normally, these functions set <b>IME_RS_ERROR</b> into <b>wParam</b>.




> [!NOTE]
> The ime.h header defines SendIMEMessageEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
