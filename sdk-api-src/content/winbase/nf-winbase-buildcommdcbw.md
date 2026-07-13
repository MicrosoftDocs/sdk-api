---
UID: NF:winbase.BuildCommDCBW
title: BuildCommDCBW function (winbase.h)
description: Fills a specified DCB structure with values specified in a device-control string. (Unicode)
helpviewer_keywords: ["BuildCommDCB", "BuildCommDCB function", "BuildCommDCBW", "_win32_buildcommdcb", "base.buildcommdcb", "winbase/BuildCommDCB", "winbase/BuildCommDCBW"]
old-location: base\buildcommdcb.htm
tech.root: base
ms.assetid: 6ecd497d-2247-4b6b-8751-c107717de434
ms.date: 12/05/2018
ms.keywords: BuildCommDCB, BuildCommDCB function, BuildCommDCBA, BuildCommDCBW, _win32_buildcommdcb, base.buildcommdcb, winbase/BuildCommDCB, winbase/BuildCommDCBA, winbase/BuildCommDCBW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildCommDCBW (Unicode) and BuildCommDCBA (ANSI)
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
 - BuildCommDCBW
 - winbase/BuildCommDCBW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - BuildCommDCB
 - BuildCommDCBA
 - BuildCommDCBW
---

# BuildCommDCBW function


## -description

Fills a specified 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure with values specified in a device-control string. The device-control string uses the syntax of the <b>mode</b> command.

## -parameters

### -param lpDef [in]

The device-control information. The function takes this string, parses it, and then sets appropriate values in the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure pointed to by <i>lpDCB</i>. 




The string must have the same form as the <b>mode</b> command's command-line arguments:

COM<i>x</i>[:][baud=<i>b</i>][parity=<i>p</i>][data=<i>d</i>][stop=<i>s</i>][to={on|off}][xon={on|off}][odsr={on|off}][octs={on|off}][dtr={on|off|hs}][rts={on|off|hs|tg}][idsr={on|off}]

The device name is optional, but it must specify a valid device if used.

For example, the following string specifies a baud rate of 1200, no parity, 8 data bits, and 1 stop bit:

<code>baud=1200 parity=N data=8 stop=1</code>

### -param lpDCB [out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure that receives the information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>BuildCommDCB</b> function adjusts only those members of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure that are specifically affected by the <i>lpDef</i> parameter, with the following exceptions:

<ul>
<li>If the specified baud rate is 110, the function sets the stop bits to 2 to remain compatible with the system's <b>mode</b> command.</li>
<li>By default, 
<b>BuildCommDCB</b> disables XON/XOFF and hardware flow control. To enable flow control, you must explicitly set the appropriate members of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure.</li>
</ul>
The 
<b>BuildCommDCB</b> function only fills in the members of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure. To apply these settings to a serial port, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a> function.

There are older and newer forms of the <b>mode</b> syntax. The 
<b>BuildCommDCB</b> function supports both forms. However, you cannot mix the two forms together.

The newer form of the <b>mode</b> syntax lets you explicitly set the values of the flow control members of the 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure. If you use an older form of the <b>mode</b> syntax, the 
<b>BuildCommDCB</b> function sets the flow control members of the 
<b>DCB</b> structure, as follows:

<ul>
<li>For a string that does not end with an x or a p: 


<ul>
<li><b>fInX</b>, <b>fOutX</b>, <b>fOutXDsrFlow</b>, and <b>fOutXCtsFlow</b> are all set to <b>FALSE</b></li>
<li><b>fDtrControl</b> is set to DTR_CONTROL_ENABLE</li>
<li><b>fRtsControl</b> is set to RTS_CONTROL_ENABLE</li>
</ul>
</li>
<li>For a string that ends with an x: 


<ul>
<li><b>fInX</b> and <b>fOutX</b> are both set to <b>TRUE</b></li>
<li><b>fOutXDsrFlow</b> and <b>fOutXCtsFlow</b> are both set to <b>FALSE</b></li>
<li><b>fDtrControl</b> is set to DTR_CONTROL_ENABLE</li>
<li><b>fRtsControl</b> is set to RTS_CONTROL_ENABLE</li>
</ul>
</li>
<li>For a string that ends with a p: 


<ul>
<li><b>fInX</b> and <b>fOutX</b> are both set to <b>FALSE</b></li>
<li><b>fOutXDsrFlow</b> and <b>fOutXCtsFlow</b> are both set to <b>TRUE</b></li>
<li><b>fDtrControl</b> is set to DTR_CONTROL_HANDSHAKE</li>
<li><b>fRtsControl</b> is set to RTS_CONTROL_HANDSHAKE</li>
</ul>
</li>
</ul>




> [!NOTE]
> The winbase.h header defines BuildCommDCB as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>
