---
UID: NF:errhandlingapi.SetErrorMode
title: SetErrorMode function (errhandlingapi.h)
description: Controls whether the system or the process handles the specified serious error types.
helpviewer_keywords: ["SEM_FAILCRITICALERRORS","SEM_NOALIGNMENTFAULTEXCEPT","SEM_NOGPFAULTERRORBOX","SEM_NOOPENFILEERRORBOX","SetErrorMode","SetErrorMode function","_win32_seterrormode","base.seterrormode","errhandlingapi/SetErrorMode"]
old-location: base\seterrormode.htm
tech.root: Debug
ms.assetid: b88f5577-9124-433c-a7e8-a7f713b7b27d
ms.date: 06/17/2024
ms.keywords: SEM_FAILCRITICALERRORS, SEM_NOALIGNMENTFAULTEXCEPT, SEM_NOGPFAULTERRORBOX, SEM_NOOPENFILEERRORBOX, SetErrorMode, SetErrorMode function, _win32_seterrormode, base.seterrormode, errhandlingapi/SetErrorMode
req.header: errhandlingapi.h
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
 - SetErrorMode
 - errhandlingapi/SetErrorMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-errorhandling-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
api_name:
 - SetErrorMode
---

# SetErrorMode function


## -description

Controls whether the system or the process handles the specified serious error types.

## -parameters

### -param uMode [in]

The process error mode. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use the system default, which displays all error dialog boxes.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_FAILCRITICALERRORS"></a><a id="sem_failcriticalerrors"></a><dl>
<dt><b>SEM_FAILCRITICALERRORS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The system does not display the critical-error-handler message box. Instead, the system sends the error to the calling process.

Best practice is  that all applications call the process-wide <b>SetErrorMode</b> function with a parameter of <b>SEM_FAILCRITICALERRORS</b> at startup.  This is to prevent error mode dialogs from hanging the application.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_NOALIGNMENTFAULTEXCEPT"></a><a id="sem_noalignmentfaultexcept"></a><dl>
<dt><b>SEM_NOALIGNMENTFAULTEXCEPT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The system automatically fixes memory alignment faults and makes them invisible to the application. It does this for the calling process and any descendant processes. This feature is only supported by certain processor architectures. For more information, see the Remarks section.
								

After this value is set for a process, subsequent attempts to clear the value are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_NOGPFAULTERRORBOX"></a><a id="sem_nogpfaulterrorbox"></a><dl>
<dt><b>SEM_NOGPFAULTERRORBOX</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The system does not invoke Windows Error Reporting. To disable Windows Error Reporting UI, call WerSetFlags with the WER_FAULT_REPORTING_NO_UI flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_NOOPENFILEERRORBOX"></a><a id="sem_noopenfileerrorbox"></a><dl>
<dt><b>SEM_NOOPENFILEERRORBOX</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a> function does not display a message box when it fails to find a file. Instead, the error is returned to the caller. This error mode overrides the <b>OF_PROMPT</b> flag.

</td>
</tr>
</table>

## -returns

The return value is the previous state of the error-mode bit flags.

## -remarks

Each process has an associated error mode that indicates to the system how the application is going to respond to serious errors. A child process inherits the error mode of its parent process. To retrieve the process error mode, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-geterrormode">GetErrorMode</a> function.

Because the error mode is set for the entire process, you must ensure that multi-threaded applications do not set different error-mode flags. Doing so can lead to inconsistent error handling.

The system does not make alignment faults visible to an application on all processor architectures. Therefore, specifying SEM_NOALIGNMENTFAULTEXCEPT is not an error on such architectures, but the system is free to silently ignore the request. This means that code sequences such as the following are not always valid on x86 computers:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SetErrorMode(SEM_NOALIGNMENTFAULTEXCEPT); 
fuOldErrorMode = SetErrorMode(0); 
ASSERT(fuOldErrorMode == SEM_NOALIGNMENTFAULTEXCEPT);</pre>
</td>
</tr>
</table></span></div>
<b>Itanium:  </b>An application must explicitly call 
<b>SetErrorMode</b> with SEM_NOALIGNMENTFAULTEXCEPT to have the system automatically fix alignment faults. The default setting is for the system to make alignment faults visible to an application.

<b>Visual Studio 2005:  </b>When declaring a pointer to a structure that may not have aligned data, you can use the <b>__unaligned</b> keyword to indicate that the type must be read one byte at a time. For more information, see <a href="https://msdn.microsoft.com/library/Aa290049.aspx">Windows Data Alignment</a>.

<b>Windows 7:  </b>Callers should favor <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode">SetThreadErrorMode</a> over <b>SetErrorMode</b> since it is less disruptive to the normal behavior of the system.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/Debug/error-mode">Error Mode</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-geterrormode">GetErrorMode</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode">SetThreadErrorMode</a>
