---
UID: NF:errorrep.ReportFault
title: ReportFault function
author: windows-driver-content
description: Enables an application that performs its own exception handling to report faults to Microsoft.
old-location: wer\reportfault.htm
old-project: wer
ms.assetid: 9f7c2abc-4d9a-4f3b-a540-e4546ed709de
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: ReportFault, ReportFault function [Windows Error Reporting], _win32_reportfault, base.reportfault, errorrep/ReportFault, wer.reportfault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Faultrep.dll
api_name:
-	ReportFault
product: Windows
targetos: Windows
req.lib: Faultrep.lib
req.dll: Faultrep.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# ReportFault function


## -description


Enables an application that performs its own exception handling to report faults to Microsoft. Although you can use this function to  report application crashes, we recommend that applications not handle fatal errors directly but instead rely on the crash reporting capability provided by the operating system.


## -parameters




### -param pep [in]

 A pointer to an 
<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure.


### -param dwOpt

TBD




#### - dwMode [in]

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




<a href="https://msdn.microsoft.com/9055437b-2ee2-4f0a-bcef-2b04ac5368b3">AddERExcludedApplication</a>



<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a>



<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

