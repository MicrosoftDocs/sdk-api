---
UID: NF:winbase.EscapeCommFunction
title: EscapeCommFunction function (winbase.h)
description: Directs the specified communications device to perform an extended function.
helpviewer_keywords: ["CLRBREAK","CLRDTR","CLRRTS","EscapeCommFunction","EscapeCommFunction function","SETBREAK","SETDTR","SETRTS","SETXOFF","SETXON","_win32_escapecommfunction","base.escapecommfunction","winbase/EscapeCommFunction"]
old-location: base\escapecommfunction.htm
tech.root: base
ms.assetid: 27c4ebdf-1c06-4a60-8e49-dcccba10789c
ms.date: 12/05/2018
ms.keywords: CLRBREAK, CLRDTR, CLRRTS, EscapeCommFunction, EscapeCommFunction function, SETBREAK, SETDTR, SETRTS, SETXOFF, SETXON, _win32_escapecommfunction, base.escapecommfunction, winbase/EscapeCommFunction
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
 - EscapeCommFunction
 - winbase/EscapeCommFunction
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
 - EscapeCommFunction
---

# EscapeCommFunction function


## -description

Directs the specified communications device to perform an extended function.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param dwFunc [in]

The extended function to be performed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLRBREAK"></a><a id="clrbreak"></a><dl>
<dt><b>CLRBREAK</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Restores character transmission and places the transmission line in a nonbreak state. The CLRBREAK extended function code is identical to the 
<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CLRDTR"></a><a id="clrdtr"></a><dl>
<dt><b>CLRDTR</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Clears the DTR (data-terminal-ready) signal.

</td>
</tr>
<tr>
<td width="40%"><a id="CLRRTS"></a><a id="clrrts"></a><dl>
<dt><b>CLRRTS</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Clears the RTS (request-to-send) signal.

</td>
</tr>
<tr>
<td width="40%"><a id="SETBREAK"></a><a id="setbreak"></a><dl>
<dt><b>SETBREAK</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Suspends character transmission and places the transmission line in a break state until the 
<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a> function is called (or 
<b>EscapeCommFunction</b> is called with the CLRBREAK extended function code). The SETBREAK extended function code is identical to the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommbreak">SetCommBreak</a> function. Note that this extended function does not flush data that has not been transmitted.

</td>
</tr>
<tr>
<td width="40%"><a id="SETDTR"></a><a id="setdtr"></a><dl>
<dt><b>SETDTR</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Sends the DTR (data-terminal-ready) signal.

</td>
</tr>
<tr>
<td width="40%"><a id="SETRTS"></a><a id="setrts"></a><dl>
<dt><b>SETRTS</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Sends the RTS (request-to-send) signal.

</td>
</tr>
<tr>
<td width="40%"><a id="SETXOFF"></a><a id="setxoff"></a><dl>
<dt><b>SETXOFF</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Causes transmission to act as if an XOFF character has been received.

</td>
</tr>
<tr>
<td width="40%"><a id="SETXON"></a><a id="setxon"></a><dl>
<dt><b>SETXON</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Causes transmission to act as if an XON character has been received.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-clearcommbreak">ClearCommBreak</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommbreak">SetCommBreak</a>