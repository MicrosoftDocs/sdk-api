---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# StopWatchMode function


## -description


<p class="CCE_Message">[<b>StopWatchMode</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a value that indicates which performance information is being logged.


## -parameters






## -returns



Type: <b>DWORD</b>

The current stopwatch mode. If performance information is not being logged, then the stopwatch mode is zero. Otherwise, it consists of one or more of the following flags.

<table class="clsStd">
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>SPMODE_SHELL</td>
<td>0x00000001</td>
<td>Logs selected Windows Explorer actions.</td>
</tr>
<tr>
<td>SPMODE_DEBUGOUT</td>
<td>0x00000002</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_TEST</td>
<td>0x00000004</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_BROWSER</td>
<td>0x00000008</td>
<td>Logs selected activities of the Windows Explorer or Internet Explorer browser frame. This flag cannot be combined with SPMODE_EVENTTRACE.</td>
</tr>
<tr>
<td>SPMODE_FLUSH</td>
<td>0x00000010</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_EVENT</td>
<td>0x00000020</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MSVM</td>
<td>0x00000040</td>
<td>Logs selected times for initializing the Microsoft VM.</td>
</tr>
<tr>
<td>SPMODE_FORMATTEXT</td>
<td>0x00000080</td>
<td>
Windows 2000: Indicates in the log which entries affect the browser frame.

Windows XP: Has no effect.

</td>
</tr>
<tr>
<td>SPMODE_PROFILE</td>
<td>0x00000100</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_DEBUGBREAK</td>
<td>0x00000200</td>
<td>Breaks into the debugger after each log entry is created. If there is no debugger available, the program halts with a STATUS_BREAKPOINT exception.</td>
</tr>
<tr>
<td>SPMODE_MSGTRACE</td>
<td>0x00000400</td>
<td>Enables message performance logs.</td>
</tr>
<tr>
<td>SPMODE_PERFTAGS</td>
<td>0x00000800</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MEMWATCH</td>
<td>0x00001000</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_DBMON</td>
<td>0x00002000</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MULTISTOP</td>
<td>0x00004000</td>
<td>Logs all "stop" operations even if there is only one matching "start".</td>
</tr>
<tr>
<td>SPMODE_EVENTTRACE</td>
<td>0x00008000</td>
<td>Logs selected activities of the MSHTML rendering engine. This flag cannot be combined with SPMODE_BROWSER.</td>
</tr>
</table>
 




## -remarks



To enable performance logging, set the following REG_DWORD registry value. You should restart your computer after setting this value, to ensure that the change has taken effect.




<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>Performance</b>
                     <b>Mode</b></pre>


The information in the performance log is intended for internal measurement purposes and the exact contents change regularly. Performance logging in its current form is subject to change in the future.

Enabling performance logging degrades performance slightly.

<div class="alert"><b>Note</b>  When using Windows XP with Service Pack 2 (SP2) and later, performance data is not collected for a process until that process calls the <b>StopWatchMode</b> function for the first time, even if the above registry value has been set to a nonzero value.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/52b79602-6e24-4d66-a400-5745149e744b">StopWatchFlush</a>
 

 

