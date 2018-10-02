---
UID: NF:winbase.BuildCommDCBW
title: BuildCommDCBW function
author: windows-sdk-content
description: Fills a specified DCB structure with values specified in a device-control string.
old-location: base\buildcommdcb.htm
tech.root: devio
ms.assetid: 6ecd497d-2247-4b6b-8751-c107717de434
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: BuildCommDCB, BuildCommDCB function, BuildCommDCBA, BuildCommDCBW, _win32_buildcommdcb, base.buildcommdcb, winbase/BuildCommDCB, winbase/BuildCommDCBA, winbase/BuildCommDCBW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BuildCommDCBW function


## -description


Fills a specified 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure with values specified in a device-control string. The device-control string uses the syntax of the <b>mode</b> command.


## -parameters




### -param lpDef [in]

The device-control information. The function takes this string, parses it, and then sets appropriate values in the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure pointed to by <i>lpDCB</i>. 




The string must have the same form as the <b>mode</b> command's command-line arguments:

COM<i>x</i>[:][baud=<i>b</i>][parity=<i>p</i>][data=<i>d</i>][stop=<i>s</i>][to={on|off}][xon={on|off}][odsr={on|off}][octs={on|off}][dtr={on|off|hs}][rts={on|off|hs|tg}][idsr={on|off}]

The device name is optional, but it must specify a valid device if used.

For example, the following string specifies a baud rate of 1200, no parity, 8 data bits, and 1 stop bit:

<code>baud=1200 parity=N data=8 stop=1</code>


### -param lpDCB [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure that receives the information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>BuildCommDCB</b> function adjusts only those members of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure that are specifically affected by the <i>lpDef</i> parameter, with the following exceptions:

<ul>
<li>If the specified baud rate is 110, the function sets the stop bits to 2 to remain compatible with the system's <b>mode</b> command.</li>
<li>By default, 
<b>BuildCommDCB</b> disables XON/XOFF and hardware flow control. To enable flow control, you must explicitly set the appropriate members of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure.</li>
</ul>
The 
<b>BuildCommDCB</b> function only fills in the members of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure. To apply these settings to a serial port, use the 
<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a> function.

There are older and newer forms of the <b>mode</b> syntax. The 
<b>BuildCommDCB</b> function supports both forms. However, you cannot mix the two forms together.

The newer form of the <b>mode</b> syntax lets you explicitly set the values of the flow control members of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure. If you use an older form of the <b>mode</b> syntax, the 
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



## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a>



<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a>
 

 

