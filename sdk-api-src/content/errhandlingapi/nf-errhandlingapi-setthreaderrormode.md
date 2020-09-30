---
UID: NF:errhandlingapi.SetThreadErrorMode
title: SetThreadErrorMode function (errhandlingapi.h)
description: Controls whether the system will handle the specified types of serious errors or whether the calling thread will handle them.
helpviewer_keywords: ["SEM_FAILCRITICALERRORS","SEM_NOGPFAULTERRORBOX","SEM_NOOPENFILEERRORBOX","SetThreadErrorMode","SetThreadErrorMode function","base.setthreaderrormode","errhandlingapi/SetThreadErrorMode"]
old-location: base\setthreaderrormode.htm
tech.root: Debug
ms.assetid: f5acb4ba-d328-47c2-8c41-17df197f12ea
ms.date: 12/05/2018
ms.keywords: SEM_FAILCRITICALERRORS, SEM_NOGPFAULTERRORBOX, SEM_NOOPENFILEERRORBOX, SetThreadErrorMode, SetThreadErrorMode function, base.setthreaderrormode, errhandlingapi/SetThreadErrorMode
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - SetThreadErrorMode
 - errhandlingapi/SetThreadErrorMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-Ms-Win-Core-ErrorHandling-L1-1-3.dll
 - KernelBase.dll
api_name:
 - SetThreadErrorMode
---

# SetThreadErrorMode function


## -description

Controls whether the system will handle the specified types of serious errors or whether the calling thread will handle them.

## -parameters

### -param dwNewMode [in]

The thread error mode. This parameter can be one or more of the following values.

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
Use the system default, which is to display all error dialog boxes.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_FAILCRITICALERRORS"></a><a id="sem_failcriticalerrors"></a><dl>
<dt><b>SEM_FAILCRITICALERRORS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The system does not display the critical-error-handler message box. Instead, the system sends the error to the calling thread.

Best practice is  that all applications call the process-wide <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a> function with a parameter of <b>SEM_FAILCRITICALERRORS</b> at startup.  This is to prevent error mode dialogs from hanging the application.

</td>
</tr>
<tr>
<td width="40%"><a id="SEM_NOGPFAULTERRORBOX"></a><a id="sem_nogpfaulterrorbox"></a><dl>
<dt><b>SEM_NOGPFAULTERRORBOX</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The system does not display the Windows Error Reporting dialog.

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

### -param lpOldMode [out]

If the function succeeds, this parameter is set to the thread's previous error mode. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Each process has an associated error mode that indicates to the system how the application is going to respond to serious errors. A thread inherits the error mode of the process in which it is running. To retrieve the process error mode, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-geterrormode">GetErrorMode</a> function. To retrieve the error mode of the calling thread, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode">GetThreadErrorMode</a> function.

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode">GetThreadErrorMode</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode">SetErrorMode</a>