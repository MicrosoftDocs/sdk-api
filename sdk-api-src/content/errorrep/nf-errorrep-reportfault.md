---
UID: NF:errorrep.ReportFault
title: ReportFault function (errorrep.h)
description: Enables an application that performs its own exception handling to report faults to Microsoft.
helpviewer_keywords: ["ReportFault","ReportFault function [Windows Error Reporting]","_win32_reportfault","base.reportfault","errorrep/ReportFault","wer.reportfault"]
old-location: wer\reportfault.htm
tech.root: wer
ms.assetid: 9f7c2abc-4d9a-4f3b-a540-e4546ed709de
ms.date: 12/05/2018
ms.keywords: ReportFault, ReportFault function [Windows Error Reporting], _win32_reportfault, base.reportfault, errorrep/ReportFault, wer.reportfault
req.header: errorrep.h
req.include-header: 
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
req.lib: Faultrep.lib
req.dll: Faultrep.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReportFault
 - errorrep/ReportFault
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Faultrep.dll
api_name:
 - ReportFault
---

# ReportFault function


## -description

Enables an application that performs its own exception handling to report faults to Microsoft. Although you can use this function to  report application crashes, we recommend that applications not handle fatal errors directly but instead rely on the crash reporting capability provided by the operating system.

## -parameters

### -param pep [in]

 A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a> structure.

### -param dwOpt [in]

This parameter is reserved for system use and should be set to zero.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvErr</b></dt>
</dl>
</td>
<td width="60%">
The function failed but the error reporting client was launched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvErrNoDW</b></dt>
</dl>
</td>
<td width="60%">
The error reporting client was unable to launch. The system will perform its default actions, such as displaying the standard exception dialog box and launching the debugger.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvErrTimeout</b></dt>
</dl>
</td>
<td width="60%">
The function timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvLaunchDebugger</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded and the user launched the debugger.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvOk</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvOkHeadless</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded and the error reporting client was launched in silent reporting mode (no UI is used).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvOkManifest</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded and the error reporting client was launched in manifest reporting mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>frrvOkQueued</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded and the fault report was queued for later reporting.

</td>
</tr>
</table>
 

These return values indicate whether the reporting application was successfully launched. A successful return value does not necessarily indicate that the fault was successfully reported.

## -remarks

The exact result of calling this function depends on how the user or system administrator has configured the error reporting system.

## -see-also

<a href="/windows/desktop/api/errorrep/nf-errorrep-adderexcludedapplicationa">AddERExcludedApplication</a>



<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a>



<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>