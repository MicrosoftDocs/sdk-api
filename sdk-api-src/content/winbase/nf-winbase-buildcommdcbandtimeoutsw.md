---
UID: NF:winbase.BuildCommDCBAndTimeoutsW
title: BuildCommDCBAndTimeoutsW function
author: windows-sdk-content
description: Translates a device-definition string into appropriate device-control block codes and places them into a device control block.
old-location: base\buildcommdcbandtimeouts.htm
old-project: DevIO
ms.assetid: d7fbc6e4-f166-4341-8ce9-37c8baab1b00
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: BuildCommDCBAndTimeouts, BuildCommDCBAndTimeouts function, BuildCommDCBAndTimeoutsA, BuildCommDCBAndTimeoutsW, _win32_buildcommdcbandtimeouts, base.buildcommdcbandtimeouts, winbase/BuildCommDCBAndTimeouts, winbase/BuildCommDCBAndTimeoutsA, winbase/BuildCommDCBAndTimeoutsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
       in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure pointed to by 
       <i>lpDCB</i>.

The string must have the same form as the <b>mode</b> command's command-line arguments:

<b>COM</b><i>x</i>[<b>:</b>][<b>baud=</b>{<b>11</b>|<b>110</b>|<b>15</b>|<b>150</b>|<b>30</b>|<b>300</b>|<b>60</b>|<b>600</b>|<b>12</b>|<b>1200</b>|<b>24</b>|<b>2400</b>|<b>48</b>|<b>4800</b>|<b>96</b>|<b>9600</b>|<b>19</b>|<b>19200</b>}][<b>parity=</b>{<b>n</b>|<b>e</b>|<b>o</b>|<b>m</b>|<b>s</b>}][<b>data=</b>{<b>5</b>|<b>6</b>|<b>7</b>|<b>8</b>}][<b>stop=</b>{<b>1</b>|<b>1.5</b>|<b>2</b>}][<b>to=</b>{<b>on</b>|<b>off</b>}][<b>xon=</b>{<b>on</b>|<b>off</b>}][<b>odsr=</b>{<b>on</b>|<b>off</b>}][<b>octs=</b>{<b>on</b>|<b>off</b>}][<b>dtr=</b>{<b>on</b>|<b>off</b>|<b>hs</b>}][<b>rts=</b>{<b>on</b>|<b>off</b>|<b>hs</b>|<b>tg</b>}][<b>idsr=</b>{<b>on</b>|<b>off</b>}]

The "baud" substring can be any of the values listed, which are in pairs. The two-digit 
       values are the first two digits of the associated values that they represent. For example, 11 represents 110 baud, 19 
       represents 19,200 baud.

The "parity" substring indicates how the parity bit is used to detect transmission errors. 
       The values represent "none", "even", "odd",        
       "mark", and "space".

For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=192055">Mode</a> command 
       reference in TechNet.

For example, the following string specifies a baud rate of 1200, no parity, 8 data bits, and 1 stop bit:

<code>baud=1200 parity=N data=8 stop=1</code>


### -param lpDCB [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure that receives information 
      from the device-control information string pointed to by <i>lpDef</i>. This 
      <b>DCB</b> structure defines the control settings for a 
      communications device.


### -param lpCommTimeouts [out]

A pointer to a <a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a> structure that 
      receives time-out information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>BuildCommDCBAndTimeouts</b> function 
    modifies its time-out setting behavior based on the presence or absence of a "to={on|off}" 
    substring in <i>lpDef</i>:

<ul>
<li>If that string contains the substring "to=on", the function sets the 
      <b>WriteTotalTimeoutConstant</b> member of the 
      <a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a> structure to 60000 and all other members 
      to 0.</li>
<li>If that string contains the substring "to=off", the function sets the members of 
      <a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a> to 0.</li>
<li>If that string does not specify a "to={on|off}" substring, the function ignores the 
      <a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a> structure in 
      <i>lpCommTimeouts</i>.</li>
</ul>
For more information, see the Remarks for the 
    <a href="https://msdn.microsoft.com/6ecd497d-2247-4b6b-8751-c107717de434">BuildCommDCB</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6ecd497d-2247-4b6b-8751-c107717de434">BuildCommDCB</a>



<a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>



<a href="https://msdn.microsoft.com/a5375b2e-0992-4e47-a20f-8a793addeef6">GetCommTimeouts</a>



<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>
 

 

