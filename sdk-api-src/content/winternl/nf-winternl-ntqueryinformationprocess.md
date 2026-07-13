---
UID: NF:winternl.NtQueryInformationProcess
title: NtQueryInformationProcess function (winternl.h)
description: Retrieves information about the specified process. (NtQueryInformationProcess)
helpviewer_keywords: ["NtQueryInformationProcess","NtQueryInformationProcess function","ProcessBasicInformation","ProcessBreakOnTermination","ProcessDebugPort","ProcessImageFileName","ProcessSubsystemInformation","ProcessWow64Information","base.ntqueryinformationprocess","winternl/NtQueryInformationProcess"]
old-location: base\ntqueryinformationprocess.htm
tech.root: backup
ms.assetid: 0eae7899-c40b-4a5f-9e9c-adae021885e7
ms.date: 12/05/2018
ms.keywords: NtQueryInformationProcess, NtQueryInformationProcess function, ProcessBasicInformation, ProcessBreakOnTermination, ProcessDebugPort, ProcessImageFileName, ProcessSubsystemInformation, ProcessWow64Information, base.ntqueryinformationprocess, winternl/NtQueryInformationProcess
req.header: winternl.h
req.include-header: 
req.target-type: Windows
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtQueryInformationProcess
 - winternl/NtQueryInformationProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtQueryInformationProcess
---

# NtQueryInformationProcess function


## -description

<p class="CCE_Message">[<b>NtQueryInformationProcess</b> may be altered or unavailable in future versions of Windows. Applications should use the alternate functions listed in this topic.]

Retrieves  information about the specified process.

## -parameters

### -param ProcessHandle [in]

A handle to the process for which information is to be retrieved.

### -param ProcessInformationClass [in]

The type of process information to be retrieved. This parameter can be one of the following values from the <b>PROCESSINFOCLASS</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ProcessBasicInformation"></a><a id="processbasicinformation"></a><a id="PROCESSBASICINFORMATION"></a><dl>
<dt><b>ProcessBasicInformation</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process. 

Use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid">GetProcessId</a>  functions to obtain this information.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessDebugPort"></a><a id="processdebugport"></a><a id="PROCESSDEBUGPORT"></a><dl>
<dt><b>ProcessDebugPort</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Retrieves a <b>DWORD_PTR</b> value that is the port number of the debugger for the process. A nonzero value indicates that the process is being run under the control of a ring 3 debugger.

Use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent">IsDebuggerPresent</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessWow64Information"></a><a id="processwow64information"></a><a id="PROCESSWOW64INFORMATION"></a><dl>
<dt><b>ProcessWow64Information</b></dt>
<dt>26</dt>
</dl>
</td>
<td width="60%">
Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).

Use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2">IsWow64Process2</a> function to obtain this information.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessImageFileName"></a><a id="processimagefilename"></a><a id="PROCESSIMAGEFILENAME"></a><dl>
<dt><b>ProcessImageFileName</b></dt>
<dt>27</dt>
</dl>
</td>
<td width="60%">
Retrieves a <b>UNICODE_STRING</b> value containing the name of the image file for the process.

Use the <a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a> or <a href="/windows/desktop/api/psapi/nf-psapi-getprocessimagefilenamea">GetProcessImageFileName</a> function to obtain this information.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessBreakOnTermination"></a><a id="processbreakontermination"></a><a id="PROCESSBREAKONTERMINATION"></a><dl>
<dt><b>ProcessBreakOnTermination</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
Retrieves a <b>ULONG</b> value indicating whether the process is considered critical.

<div class="alert"><b>Note</b>  This value can be used starting in Windows XP with SP3. Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical">IsProcessCritical</a> should be used instead.</div>
<div> </div>
</td>
</tr>

<tr>
<td width="40%"><a id="processtelemetryidinformation"></a><a id="processtelemetryidinformation"></a><a id="PROCESSTELEMETRYIDINFORMATION"></a><dl>
<dt><b>ProcessTelemetryIdInformation</b></dt>
<dt>64</dt>
</dl>
</td>
<td width="60%">


Retrieves a <b><a href="/windows/win32/devnotes/process_telemetry_id_information_type">PROCESS_TELEMETRY_ID_INFORMATION_TYPE</a></b> value that contains metadata about a process.
</td>
</tr>



<tr>
<td width="40%"><a id="ProcessSubsystemInformation"></a><a id="processsubsysteminformation"></a><a id="PROCESSSUBSYSTEMINFORMATION"></a><dl>
<dt><b>ProcessSubsystemInformation</b></dt>
<dt>75</dt>
</dl>
</td>
<td width="60%">
Retrieves a <b>SUBSYSTEM_INFORMATION_TYPE</b> value indicating the subsystem type of the process. The buffer pointed to by the <i>ProcessInformation</i> parameter should be large enough to hold a single <a href="/windows-hardware/drivers/ddi/content/ntddk/ne-ntddk-_subsystem_information_type">SUBSYSTEM_INFORMATION_TYPE</a> enumeration.

</td>
</tr>
</table>

### -param ProcessInformation [out]

A pointer to a buffer supplied by the calling application into which the function writes the requested information. The size of the information written varies depending on the data type of the <i>ProcessInformationClass</i> parameter:





#### PROCESS_BASIC_INFORMATION

When the <i>ProcessInformationClass</i>  parameter is <b>ProcessBasicInformation</b>,  the buffer pointed to by the <i>ProcessInformation</i> parameter should be large enough to hold a single <b>PROCESS_BASIC_INFORMATION</b> structure having the following layout:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    NTSTATUS ExitStatus;
    PPEB PebBaseAddress;
    ULONG_PTR AffinityMask;
    KPRIORITY BasePriority;
    ULONG_PTR UniqueProcessId;
    ULONG_PTR InheritedFromUniqueProcessId;
} PROCESS_BASIC_INFORMATION;
```

| Field | Meaning |
|-------|---------|
| **ExitStatus** | Contains the same value that [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) returns. However the use of **GetExitCodeProcess** is preferable for clarity and safety. |
| **PebBaseAddress** | Points to a [**PEB**](/windows/desktop/api/winternl/ns-winternl-peb) structure. |
| **AffinityMask** | Can be cast to a **DWORD** and contains the same value that [**GetProcessAffinityMask**](/windows/win32/api/winbase/nf-winbase-getprocessaffinitymask) returns for the `lpProcessAffinityMask` parameter. |
| **BasePriority** | Contains the process priority as described in [Scheduling Priorities](/windows/win32/procthread/scheduling-priorities#base-priority). |
| **UniqueProcessId** | Can be cast to a **DWORD** and contains a unique identifier for this process. We recommend using the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information. |
| **InheritedFromUniqueProcessId** | Can be cast to a **DWORD** and contains a unique identifier for the parent process. |



#### ULONG_PTR

When the <i>ProcessInformationClass</i>  parameter is <b>ProcessWow64Information</b>,  the buffer pointed to by the <i>ProcessInformation</i> parameter should be large enough to hold a  <b>ULONG_PTR</b>. If this value is nonzero, the process is running in a WOW64 environment. Otherwise, the process is not running in a WOW64 environment.

Use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2">IsWow64Process2</a> function to determine whether a process is running in the WOW64 environment.



#### UNICODE_STRING

When the <i>ProcessInformationClass</i>  parameter is <b>ProcessImageFileName</b>,  the buffer pointed to by the <i>ProcessInformation</i> parameter should be large enough to hold a  <b>UNICODE_STRING</b> structure as well as the string itself. The string stored in the <b>Buffer</b> member is the name of the image file.

If the buffer is too small, the function fails with the STATUS_INFO_LENGTH_MISMATCH error code and the <i>ReturnLength</i> parameter is set to the required buffer size.

### -param ProcessInformationLength [in]

The size of the buffer pointed to by the <i>ProcessInformation</i> parameter, in bytes.

### -param ReturnLength [out, optional]

A pointer to a variable in which the function returns the size of the requested information. If the function was successful, this is the size of the information written to the buffer pointed to by the <i>ProcessInformation</i> parameter (if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully).

## -returns

The function returns an NTSTATUS success or error code. 

The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK. See [Logging Errors](/windows-hardware/drivers/kernel/logging-errors) for more details.

## -remarks

The <b>NtQueryInformationProcess</b> function and the structures that it returns are internal to the operating system and  subject to change from one  release of Windows to another.  To maintain the    compatibility of your application, it is better to use public functions mentioned in the description of the <i>ProcessInformationClass</i> parameter instead.

If you do use <b>NtQueryInformationProcess</b>, access the function through <a href="/windows/desktop/Dlls/using-run-time-dynamic-linking">run-time dynamic linking</a>.  This gives  your code an opportunity to respond gracefully if the function has been   changed or removed from the operating system. Signature changes, however, may not be detectable.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

## -see-also

<a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid">GetProcessId</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent">IsDebuggerPresent</a>



<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process">IsWow64Process</a>



<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2">IsWow64Process2</a>
