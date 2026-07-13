---
UID: NF:winbase.BuildCommDCBAndTimeoutsW
title: BuildCommDCBAndTimeoutsW function (winbase.h)
description: Translates a device-definition string into appropriate device-control block codes and places them into a device control block. (Unicode)
helpviewer_keywords: ["BuildCommDCBAndTimeouts", "BuildCommDCBAndTimeouts function", "BuildCommDCBAndTimeoutsW", "_win32_buildcommdcbandtimeouts", "base.buildcommdcbandtimeouts", "winbase/BuildCommDCBAndTimeouts", "winbase/BuildCommDCBAndTimeoutsW"]
old-location: base\buildcommdcbandtimeouts.htm
tech.root: base
ms.assetid: d7fbc6e4-f166-4341-8ce9-37c8baab1b00
ms.date: 12/05/2018
ms.keywords: BuildCommDCBAndTimeouts, BuildCommDCBAndTimeouts function, BuildCommDCBAndTimeoutsA, BuildCommDCBAndTimeoutsW, _win32_buildcommdcbandtimeouts, base.buildcommdcbandtimeouts, winbase/BuildCommDCBAndTimeouts, winbase/BuildCommDCBAndTimeoutsA, winbase/BuildCommDCBAndTimeoutsW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildCommDCBAndTimeoutsW (Unicode) and BuildCommDCBAndTimeoutsA (ANSI)
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
 - BuildCommDCBAndTimeoutsW
 - winbase/BuildCommDCBAndTimeoutsW
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
 - BuildCommDCBAndTimeouts
 - BuildCommDCBAndTimeoutsA
 - BuildCommDCBAndTimeoutsW
---

# BuildCommDCBAndTimeoutsW function


## -description

Translates a device-definition string into appropriate device-control block codes and places them into 
    a device control block. The function can also set up time-out values, including the possibility of no 
    time-outs, for a device; the function's behavior in this regard depends on the contents of the device-definition 
    string.

## -parameters

### -param lpDef [in]

The device-control information. The function takes this string, parses it, and then sets appropriate values 
       in the <a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure pointed to by 
       <i>lpDCB</i>.

The string must have the same form as the <b>mode</b> command's command-line arguments:

<b>COM</b><i>x</i>[<b>:</b>][<b>baud=</b>{<b>11</b>|<b>110</b>|<b>15</b>|<b>150</b>|<b>30</b>|<b>300</b>|<b>60</b>|<b>600</b>|<b>12</b>|<b>1200</b>|<b>24</b>|<b>2400</b>|<b>48</b>|<b>4800</b>|<b>96</b>|<b>9600</b>|<b>19</b>|<b>19200</b>}][<b>parity=</b>{<b>n</b>|<b>e</b>|<b>o</b>|<b>m</b>|<b>s</b>}][<b>data=</b>{<b>5</b>|<b>6</b>|<b>7</b>|<b>8</b>}][<b>stop=</b>{<b>1</b>|<b>1.5</b>|<b>2</b>}][<b>to=</b>{<b>on</b>|<b>off</b>}][<b>xon=</b>{<b>on</b>|<b>off</b>}][<b>odsr=</b>{<b>on</b>|<b>off</b>}][<b>octs=</b>{<b>on</b>|<b>off</b>}][<b>dtr=</b>{<b>on</b>|<b>off</b>|<b>hs</b>}][<b>rts=</b>{<b>on</b>|<b>off</b>|<b>hs</b>|<b>tg</b>}][<b>idsr=</b>{<b>on</b>|<b>off</b>}]

The "baud" substring can be any of the values listed, which are in pairs. The two-digit 
       values are the first two digits of the associated values that they represent. For example, 11 represents 110 baud, 19 
       represents 19,200 baud.

The "parity" substring indicates how the parity bit is used to detect transmission errors. 
       The values represent "none", "even", "odd",        
       "mark", and "space".

For more information, see the <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732236(v=ws.11)">Mode</a> command 
       reference in TechNet.

For example, the following string specifies a baud rate of 1200, no parity, 8 data bits, and 1 stop bit:

<code>baud=1200 parity=N data=8 stop=1</code>

### -param lpDCB [out]

A pointer to a <a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure that receives information 
      from the device-control information string pointed to by <i>lpDef</i>. This 
      <b>DCB</b> structure defines the control settings for a 
      communications device.

### -param lpCommTimeouts [out]

A pointer to a <a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> structure that 
      receives time-out information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>BuildCommDCBAndTimeouts</b> function 
    modifies its time-out setting behavior based on the presence or absence of a "to={on|off}" 
    substring in <i>lpDef</i>:

<ul>
<li>If that string contains the substring "to=on", the function sets the 
      <b>WriteTotalTimeoutConstant</b> member of the 
      <a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> structure to 60000 and all other members 
      to 0.</li>
<li>If that string contains the substring "to=off", the function sets the members of 
      <a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> to 0.</li>
<li>If that string does not specify a "to={on|off}" substring, the function ignores the 
      <a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a> structure in 
      <i>lpCommTimeouts</i>.</li>
</ul>
For more information, see the Remarks for the 
    <a href="/windows/desktop/api/winbase/nf-winbase-buildcommdcba">BuildCommDCB</a> function.





> [!NOTE]
> The winbase.h header defines BuildCommDCBAndTimeouts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-buildcommdcba">BuildCommDCB</a>



<a href="/windows/desktop/api/winbase/ns-winbase-commtimeouts">COMMTIMEOUTS</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommtimeouts">GetCommTimeouts</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>
