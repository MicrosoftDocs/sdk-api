---
UID: NF:winbase.ClearCommError
title: ClearCommError function (winbase.h)
description: Retrieves information about a communications error and reports the current status of a communications device.
helpviewer_keywords: ["CE_BREAK","CE_FRAME","CE_OVERRUN","CE_RXOVER","CE_RXPARITY","ClearCommError","ClearCommError function","_win32_clearcommerror","base.clearcommerror","winbase/ClearCommError"]
old-location: base\clearcommerror.htm
tech.root: base
ms.assetid: 9cc52104-aa5e-4baa-86f1-8c6dcdd661ef
ms.date: 12/05/2018
ms.keywords: CE_BREAK, CE_FRAME, CE_OVERRUN, CE_RXOVER, CE_RXPARITY, ClearCommError, ClearCommError function, _win32_clearcommerror, base.clearcommerror, winbase/ClearCommError
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClearCommError
 - winbase/ClearCommError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ClearCommError
---

# ClearCommError function


## -description

Retrieves information about a communications error and reports the current status of a communications device. The function is called when a communications error occurs, and it clears the device's error flag to enable additional input and output (I/O) operations.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpErrors [out, optional]

A pointer to a variable that receives a mask indicating the type of error. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CE_BREAK"></a><a id="ce_break"></a><dl>
<dt><b>CE_BREAK</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The hardware detected a break condition.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_FRAME"></a><a id="ce_frame"></a><dl>
<dt><b>CE_FRAME</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The hardware detected a framing error.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_OVERRUN"></a><a id="ce_overrun"></a><dl>
<dt><b>CE_OVERRUN</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A character-buffer overrun has occurred. The next character is lost.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_RXOVER"></a><a id="ce_rxover"></a><dl>
<dt><b>CE_RXOVER</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
An input buffer overflow has occurred. There is either no room in the input buffer, or a character was received after the end-of-file (EOF) character.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_RXPARITY"></a><a id="ce_rxparity"></a><dl>
<dt><b>CE_RXPARITY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The hardware detected a parity error.

</td>
</tr>
</table>
 

The following values are not supported:

### -param lpStat [out, optional]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-comstat">COMSTAT</a> structure in which the device's status information is returned. If this parameter is <b>NULL</b>, no status information is returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a communications port has been set up with a <b>TRUE</b> value for the <b>fAbortOnError</b> member of the setup 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure, the communications software will terminate all read and write operations on the communications port when a communications error occurs. No new read or write operations will be accepted until the application acknowledges the communications error by calling the 
<b>ClearCommError</b> function.

The 
<b>ClearCommError</b> function fills the status buffer pointed to by the <i>lpStat</i> parameter with the current status of the communications device specified by the <i>hFile</i> parameter.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-comstat">COMSTAT</a>



<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>