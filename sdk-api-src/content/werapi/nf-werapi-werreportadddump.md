---
UID: NF:werapi.WerReportAddDump
title: WerReportAddDump function
author: windows-sdk-content
description: Adds a dump of the specified type to the specified report.
old-location: wer\werreportadddump.htm
tech.root: wer
ms.assetid: b40dac44-f7c5-43f0-876d-6f97c26bf461
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WER_DUMP_NOHEAP_ONQUEUE, WerDumpTypeHeapDump, WerDumpTypeMicroDump, WerDumpTypeMiniDump, WerReportAddDump, WerReportAddDump function [Windows Error Reporting], base.werreportadddump, wer.werreportadddump, werapi/WerReportAddDump
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
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
 - WerReportAddDump
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerReportAddDump function


## -description


Adds a dump of the specified type to the specified report.


## -parameters




### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a> function.


### -param hProcess [in]

A handle to the process for which the report is being generated. This handle must have the STANDARD_RIGHTS_READ and PROCESS_QUERY_INFORMATION access rights.


### -param hThread [in, optional]

A handle to the thread of <i>hProcess</i> for which the report is being generated. If <i>dumpType</i> is WerDumpTypeMicro, this parameter is required. For other dump types, this parameter may be <b>NULL</b>.


### -param dumpType [in]

The type of <a href="https://msdn.microsoft.com/c5de86a4-6dab-4408-8093-66117eb4de10">minidump</a>. This parameter can be one of the following values from the <b>WER_DUMP_TYPE</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WerDumpTypeHeapDump"></a><a id="werdumptypeheapdump"></a><a id="WERDUMPTYPEHEAPDUMP"></a><dl>
<dt><b>WerDumpTypeHeapDump</b></dt>
</dl>
</td>
<td width="60%">
An extended minidump that contains additional data such as the process memory. 

This type is equivalent to creating a minidump with the following options: <ul>
<li>MiniDumpWithDataSegs</li>
<li>MiniDumpWithProcessThreadData</li>
<li>MiniDumpWithHandleData</li>
<li>MiniDumpWithPrivateReadWriteMemory</li>
<li>MiniDumpWithUnloadedModules</li>
<li>MiniDumpWithFullMemoryInfo</li>
<li>MiniDumpWithThreadInfo (Windows 7 and later)</li>
<li>MiniDumpWithTokenInformation (Windows 7 and later)</li>
<li>MiniDumpWithPrivateWriteCopyMemory (Windows 7 and later)</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="WerDumpTypeMicroDump"></a><a id="werdumptypemicrodump"></a><a id="WERDUMPTYPEMICRODUMP"></a><dl>
<dt><b>WerDumpTypeMicroDump</b></dt>
</dl>
</td>
<td width="60%">
A limited minidump that contains only a stack trace. 

This type is equivalent to creating a minidump with the following options: <ul>
<li>MiniDumpWithDataSegs</li>
<li>MiniDumpWithUnloadedModules</li>
<li>MiniDumpWithProcessThreadData</li>
<li>MiniDumpWithoutOptionalData</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="WerDumpTypeMiniDump"></a><a id="werdumptypeminidump"></a><a id="WERDUMPTYPEMINIDUMP"></a><dl>
<dt><b>WerDumpTypeMiniDump</b></dt>
</dl>
</td>
<td width="60%">
A minidump. 

This type is equivalent to creating a minidump with the following options: <ul>
<li>MiniDumpWithDataSegs</li>
<li>MiniDumpWithUnloadedModules</li>
<li>MiniDumpWithProcessThreadData</li>
<li>MiniDumpWithTokenInformation (Windows 7 and later)</li>
</ul>


</td>
</tr>
</table>
 


### -param pExceptionParam [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4548068a-e654-40c9-9654-c5178575b42c">WER_EXCEPTION_INFORMATION</a> structure that specifies exception information.


### -param pDumpCustomOptions [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/6ea32573-ac1a-4f9b-b4ba-b5767927924f">WER_DUMP_CUSTOM_OPTIONS</a> structure that specifies custom minidump options. If this parameter is <b>NULL</b>, the standard minidump information is collected.


### -param dwFlags [in]

This parameter can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WER_DUMP_NOHEAP_ONQUEUE"></a><a id="wer_dump_noheap_onqueue"></a><dl>
<dt><b>WER_DUMP_NOHEAP_ONQUEUE</b></dt>
</dl>
</td>
<td width="60%">
If the report is being queued, do not include a heap dump. Using this flag saves disk space.

</td>
</tr>
</table>
 


## -returns



This function returns <b>S_OK</b> on success or an error code on failure.




## -remarks



Use this function only for generic reporting—it has no effect on operating system crash or no-response reporting.

If the server asks for a mini dump and you specify <b>WerDumpTypeHeapDump</b> for the <i>dumpType</i> parameter, WER will not send the heap dump to the Watson server. However, if the server asks for a heap dump and the <i>dumpType</i> is <b>WerDumpTypeMiniDump</b>, WER will send the mini dump to the server. Thus, it is recommended that you set <i>dumpType</i> to <b>WerDumpTypeMiniDump</b>.




## -see-also




<a href="https://msdn.microsoft.com/c5de86a4-6dab-4408-8093-66117eb4de10">Minidump Files</a>



<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/6ea32573-ac1a-4f9b-b4ba-b5767927924f">WER_DUMP_CUSTOM_OPTIONS</a>



<a href="https://msdn.microsoft.com/4548068a-e654-40c9-9654-c5178575b42c">WER_EXCEPTION_INFORMATION</a>



<a href="https://msdn.microsoft.com/41f68dde-5e43-45a6-8e0b-3ae0c6180e8b">WerReportCreate</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

