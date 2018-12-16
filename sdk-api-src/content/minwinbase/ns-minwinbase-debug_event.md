---
UID: NS:minwinbase._DEBUG_EVENT
title: DEBUG_EVENT
author: windows-sdk-content
description: Describes a debugging event.
old-location: base\debug_event_str.htm
tech.root: debug
ms.assetid: 056aa7ee-51ca-48ec-9cd7-26085bb85b11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDEBUG_EVENT, CREATE_PROCESS_DEBUG_EVENT, CREATE_THREAD_DEBUG_EVENT, DEBUG_EVENT, DEBUG_EVENT structure, EXCEPTION_DEBUG_EVENT, EXIT_PROCESS_DEBUG_EVENT, EXIT_THREAD_DEBUG_EVENT, LOAD_DLL_DEBUG_EVENT, LPDEBUG_EVENT, LPDEBUG_EVENT structure pointer, OUTPUT_DEBUG_STRING_EVENT, RIP_EVENT, UNLOAD_DLL_DEBUG_EVENT, _win32_debug_event_str, base.debug_event_str, minwinbase/DEBUG_EVENT, minwinbase/LPDEBUG_EVENT"
ms.topic: struct
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - DEBUG_EVENT
product: Windows
targetos: Windows
req.typenames: DEBUG_EVENT, *LPDEBUG_EVENT
req.redist: 
---

# DEBUG_EVENT structure


## -description


Describes a debugging event.


## -struct-fields




### -field dwDebugEventCode

Type: <b>DWORD</b>

The code that identifies the type of debugging event. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_PROCESS_DEBUG_EVENT"></a><a id="create_process_debug_event"></a><dl>
<dt><b>CREATE_PROCESS_DEBUG_EVENT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Reports a create-process debugging event. The value of <b>u.CreateProcessInfo</b> 
        specifies a <a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a> 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_THREAD_DEBUG_EVENT"></a><a id="create_thread_debug_event"></a><dl>
<dt><b>CREATE_THREAD_DEBUG_EVENT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Reports a create-thread debugging event. The value of <b>u.CreateThread</b> specifies 
        a <a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a> 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="EXCEPTION_DEBUG_EVENT"></a><a id="exception_debug_event"></a><dl>
<dt><b>EXCEPTION_DEBUG_EVENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Reports an exception debugging event. The value of <b>u.Exception</b> specifies an 
        <a href="https://msdn.microsoft.com/f5917ae3-cc45-42c4-a3fb-5d0aef2a3bdb">EXCEPTION_DEBUG_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="EXIT_PROCESS_DEBUG_EVENT"></a><a id="exit_process_debug_event"></a><dl>
<dt><b>EXIT_PROCESS_DEBUG_EVENT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Reports an exit-process debugging event. The value of <b>u.ExitProcess</b> specifies 
        an <a href="https://msdn.microsoft.com/91a7f4bf-88c7-4a57-b0d0-0d379d967baf">EXIT_PROCESS_DEBUG_INFO</a> 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="EXIT_THREAD_DEBUG_EVENT"></a><a id="exit_thread_debug_event"></a><dl>
<dt><b>EXIT_THREAD_DEBUG_EVENT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Reports an exit-thread debugging event. The value of <b>u.ExitThread</b> specifies an 
        <a href="https://msdn.microsoft.com/8c135992-2adc-4c7a-bd64-130d4d8ef16c">EXIT_THREAD_DEBUG_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="LOAD_DLL_DEBUG_EVENT"></a><a id="load_dll_debug_event"></a><dl>
<dt><b>LOAD_DLL_DEBUG_EVENT</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Reports a load-dynamic-link-library (DLL) debugging event. The value of 
        <b>u.LoadDll</b> specifies a 
        <a href="https://msdn.microsoft.com/80edb12f-1d1f-4480-9032-5f7a17f47910">LOAD_DLL_DEBUG_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="OUTPUT_DEBUG_STRING_EVENT"></a><a id="output_debug_string_event"></a><dl>
<dt><b>OUTPUT_DEBUG_STRING_EVENT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Reports an output-debugging-string debugging event. The value of <b>u.DebugString</b> 
        specifies an <a href="https://msdn.microsoft.com/43594bf5-ee79-4334-b0d4-92b2b41bf35a">OUTPUT_DEBUG_STRING_INFO</a> 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RIP_EVENT"></a><a id="rip_event"></a><dl>
<dt><b>RIP_EVENT</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Reports a RIP-debugging event (system debugging error). The value of <b>u.RipInfo</b> 
        specifies a <a href="https://msdn.microsoft.com/2aef4de7-bf3d-4add-9801-e26081f0f76b">RIP_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="UNLOAD_DLL_DEBUG_EVENT"></a><a id="unload_dll_debug_event"></a><dl>
<dt><b>UNLOAD_DLL_DEBUG_EVENT</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Reports an unload-DLL debugging event. The value of <b>u.UnloadDll</b> specifies an 
        <a href="https://msdn.microsoft.com/a4ece775-a49e-406b-8eae-264f978eb597">UNLOAD_DLL_DEBUG_INFO</a> structure.

</td>
</tr>
</table>
 


### -field dwProcessId

Type: <b>DWORD</b>

The identifier of the process in which the debugging event occurred. A debugger uses this value to locate 
      the debugger's per-process structure. These values are not necessarily small integers that can be used as table 
      indices.


### -field dwThreadId

Type: <b>DWORD</b>

The identifier of the thread in which the debugging event occurred. A debugger uses this value to locate 
      the debugger's per-thread structure. These values are not necessarily small integers that can be used as table 
      indices.


### -field u

Any additional information relating to the debugging event. This union takes on the type and value 
      appropriate to the type of debugging event, as described in the <b>dwDebugEventCode</b> 
      member.


### -field u.Exception

<b>Type: <b><a href="https://msdn.microsoft.com/f5917ae3-cc45-42c4-a3fb-5d0aef2a3bdb">EXCEPTION_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>EXCEPTION_DEBUG_EVENT</b> (1), 
       <b>u.Exception</b> specifies an 
       <a href="https://msdn.microsoft.com/f5917ae3-cc45-42c4-a3fb-5d0aef2a3bdb">EXCEPTION_DEBUG_INFO</a> structure.


### -field u.CreateThread

<b>Type: <b><a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>CREATE_THREAD_DEBUG_EVENT</b> 
       (2), <b>u.CreateThread</b> specifies an 
       <a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a> 
       structure.


### -field u.CreateProcessInfo

<b>Type: <b><a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>CREATE_PROCESS_DEBUG_EVENT</b> 
       (3), <b>u.CreateProcessInfo</b> specifies an 
       <a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a> 
       structure.


### -field u.ExitThread

<b>Type: <b><a href="https://msdn.microsoft.com/8c135992-2adc-4c7a-bd64-130d4d8ef16c">EXIT_THREAD_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>EXIT_THREAD_DEBUG_EVENT</b> 
       (4), <b>u.ExitThread</b> specifies an 
       <a href="https://msdn.microsoft.com/8c135992-2adc-4c7a-bd64-130d4d8ef16c">EXIT_THREAD_DEBUG_INFO</a> structure.


### -field u.ExitProcess

<b>Type: <b><a href="https://msdn.microsoft.com/91a7f4bf-88c7-4a57-b0d0-0d379d967baf">EXIT_PROCESS_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>EXIT_PROCESS_DEBUG_EVENT</b> 
       (5), <b>u.ExitProcess</b> specifies an 
       <a href="https://msdn.microsoft.com/91a7f4bf-88c7-4a57-b0d0-0d379d967baf">EXIT_PROCESS_DEBUG_INFO</a> structure.


### -field u.LoadDll

<b>Type: <b><a href="https://msdn.microsoft.com/80edb12f-1d1f-4480-9032-5f7a17f47910">LOAD_DLL_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>LOAD_DLL_DEBUG_EVENT</b> (6), 
       <b>u.LoadDll</b> specifies an 
       <a href="https://msdn.microsoft.com/80edb12f-1d1f-4480-9032-5f7a17f47910">LOAD_DLL_DEBUG_INFO</a> structure.


### -field u.UnloadDll

<b>Type: <b><a href="https://msdn.microsoft.com/a4ece775-a49e-406b-8eae-264f978eb597">UNLOAD_DLL_DEBUG_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>UNLOAD_DLL_DEBUG_EVENT</b> 
       (7), <b>u.UnloadDll</b> specifies an 
       <a href="https://msdn.microsoft.com/a4ece775-a49e-406b-8eae-264f978eb597">UNLOAD_DLL_DEBUG_INFO</a> structure.


### -field u.DebugString

<b>Type: <b><a href="https://msdn.microsoft.com/43594bf5-ee79-4334-b0d4-92b2b41bf35a">OUTPUT_DEBUG_STRING_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>OUTPUT_DEBUG_STRING_EVENT</b> 
       (8), <b>u.DebugString</b> specifies an 
       <a href="https://msdn.microsoft.com/43594bf5-ee79-4334-b0d4-92b2b41bf35a">OUTPUT_DEBUG_STRING_INFO</a> 
       structure.


### -field u.RipInfo

<b>Type: <b><a href="https://msdn.microsoft.com/2aef4de7-bf3d-4add-9801-e26081f0f76b">RIP_INFO</a></b>
</b>
If the <b>dwDebugEventCode</b> is <b>RIP_EVENT</b> (9), 
       <b>u.RipInfo</b> specifies an 
       <a href="https://msdn.microsoft.com/2aef4de7-bf3d-4add-9801-e26081f0f76b">RIP_INFO</a> structure.


## -remarks



If the <a href="https://msdn.microsoft.com/0d81a4ac-dd66-4648-9f3f-1f54aca84243">WaitForDebugEvent</a> function succeeds, it 
    fills in the members of a <b>DEBUG_EVENT</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/f5917ae3-cc45-42c4-a3fb-5d0aef2a3bdb">EXCEPTION_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/91a7f4bf-88c7-4a57-b0d0-0d379d967baf">EXIT_PROCESS_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/8c135992-2adc-4c7a-bd64-130d4d8ef16c">EXIT_THREAD_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/80edb12f-1d1f-4480-9032-5f7a17f47910">LOAD_DLL_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/43594bf5-ee79-4334-b0d4-92b2b41bf35a">OUTPUT_DEBUG_STRING_INFO</a>



<a href="https://msdn.microsoft.com/a4ece775-a49e-406b-8eae-264f978eb597">UNLOAD_DLL_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/0d81a4ac-dd66-4648-9f3f-1f54aca84243">WaitForDebugEvent</a>
 

 

