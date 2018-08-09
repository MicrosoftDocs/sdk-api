---
UID: NF:werapi.WerReportCreate
title: WerReportCreate function
author: windows-sdk-content
description: Creates a problem report that describes an application event.
old-location: wer\werreportcreate.htm
old-project: wer
ms.assetid: 41f68dde-5e43-45a6-8e0b-3ae0c6180e8b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WerReportApplicationCrash, WerReportApplicationHang, WerReportCreate, WerReportCreate function [Windows Error Reporting], WerReportCritical, WerReportInvalid, WerReportKernel, WerReportNonCritical, base.werreportcreate, wer.werreportcreate, werapi/WerReportCreate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportCreate
product: Windows
targetos: Windows
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerReportCreate function


## -description


Creates a problem report that describes an application event.


## -parameters




### -param pwzEventType [in]

A pointer to a Unicode string that specifies the name of the event.


### -param repType [in]

The type of report. This parameter can be one of the following values from the <b>WER_REPORT_TYPE</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerReportApplicationCrash"></a><a id="werreportapplicationcrash"></a><a id="WERREPORTAPPLICATIONCRASH"></a><dl>
<dt><b>WerReportApplicationCrash</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An error that has caused the application to stop running has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportApplicationHang"></a><a id="werreportapplicationhang"></a><a id="WERREPORTAPPLICATIONHANG"></a><dl>
<dt><b>WerReportApplicationHang</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
An error that has caused the application to stop responding has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportInvalid"></a><a id="werreportinvalid"></a><a id="WERREPORTINVALID"></a><dl>
<dt><b>WerReportInvalid</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
An error that has called out a return that is not valid has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportKernel"></a><a id="werreportkernel"></a><a id="WERREPORTKERNEL"></a><dl>
<dt><b>WerReportKernel</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
An error in the kernel has occurred. 

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportCritical"></a><a id="werreportcritical"></a><a id="WERREPORTCRITICAL"></a><dl>
<dt><b>WerReportCritical</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A critical error, such as a crash or non-response, has occurred. By default, processes that experience a critical error are terminated or restarted.

</td>
</tr>
<tr>
<td width="40%"><a id="WerReportNonCritical"></a><a id="werreportnoncritical"></a><a id="WERREPORTNONCRITICAL"></a><dl>
<dt><b>WerReportNonCritical</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An error that is not critical has occurred. This type of report shows no UI; the report is silently queued. It may then be sent silently to the server in the background if adequate user consent is available.

</td>
</tr>
</table>
 


### -param pReportInformation [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3efe2b43-53ac-48e3-bc39-4a9fe6041fca">WER_REPORT_INFORMATION</a> structure that specifies information for the report.


### -param phReportHandle [out]

A handle to the report. If the function fails, this handle is <b>NULL</b>.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure.




## -remarks



Use the following functions to specify additional information to be submitted:

<a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a>
<a href="https://msdn.microsoft.com/4b2c2060-a193-4168-90fc-afb95c160569">WerReportAddFile</a>
<a href="https://msdn.microsoft.com/accf423d-6f03-41e2-b5e9-4a0b630bc918">WerReportSetParameter</a>
To submit the information, call the <a href="https://msdn.microsoft.com/1433862e-5cf6-4d31-9fd9-137b7b86ec57">WerReportSubmit</a> function. When you have finished with the report handle, call the <a href="https://msdn.microsoft.com/b7326003-cd25-4988-9ed4-31c2e030beec">WerReportCloseHandle</a> function.

Applications can also indicate that they would like the opportunity to recover data or restart on failure. For more information, see <a href="https://msdn.microsoft.com/9357786c-1992-4e28-ac75-c2dfda1df7f1">Application Recovery and Restart</a>.

To view the reports submitted by your application, go to <a href="Http://go.microsoft.com/fwlink/p/?linkid=84169">Windows Quality Online Services</a>.




## -see-also




<a href="https://msdn.microsoft.com/9357786c-1992-4e28-ac75-c2dfda1df7f1">Application Recovery and Restart</a>



<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/3efe2b43-53ac-48e3-bc39-4a9fe6041fca">WER_REPORT_INFORMATION</a>



<a href="https://msdn.microsoft.com/b7326003-cd25-4988-9ed4-31c2e030beec">WerReportCloseHandle</a>



<a href="https://msdn.microsoft.com/1433862e-5cf6-4d31-9fd9-137b7b86ec57">WerReportSubmit</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

