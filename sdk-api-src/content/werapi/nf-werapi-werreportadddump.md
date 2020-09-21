---
UID: NF:werapi.WerReportAddDump
title: WerReportAddDump function (werapi.h)
description: Adds a dump of the specified type to the specified report.
helpviewer_keywords: ["WER_DUMP_NOHEAP_ONQUEUE","WerDumpTypeHeapDump","WerDumpTypeMicroDump","WerDumpTypeMiniDump","WerReportAddDump","WerReportAddDump function [Windows Error Reporting]","base.werreportadddump","wer.werreportadddump","werapi/WerReportAddDump"]
old-location: wer\werreportadddump.htm
tech.root: wer
ms.assetid: b40dac44-f7c5-43f0-876d-6f97c26bf461
ms.date: 12/05/2018
ms.keywords: WER_DUMP_NOHEAP_ONQUEUE, WerDumpTypeHeapDump, WerDumpTypeMicroDump, WerDumpTypeMiniDump, WerReportAddDump, WerReportAddDump function [Windows Error Reporting], base.werreportadddump, wer.werreportadddump, werapi/WerReportAddDump
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerReportAddDump
 - werapi/WerReportAddDump
dev_langs:
 - c++
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
---

# WerReportAddDump function


## -description

Adds a dump of the specified type to the specified report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the <a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a> function.

### -param hProcess [in]

A handle to the process for which the report is being generated. This handle must have the STANDARD_RIGHTS_READ and PROCESS_QUERY_INFORMATION access rights.

### -param hThread [in, optional]

A handle to the thread of <i>hProcess</i> for which the report is being generated. If <i>dumpType</i> is WerDumpTypeMicro, this parameter is required. For other dump types, this parameter may be <b>NULL</b>.

### -param dumpType [in]

The type of <a href="/windows/desktop/Debug/minidump-files">minidump</a>. This parameter can be one of the following values from the <b>WER_DUMP_TYPE</b> enumeration type.

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

A pointer to a <a href="/windows/desktop/api/werapi/ns-werapi-wer_exception_information">WER_EXCEPTION_INFORMATION</a> structure that specifies exception information.

### -param pDumpCustomOptions [in, optional]

A pointer to a <a href="/windows/desktop/api/werapi/ns-werapi-wer_dump_custom_options">WER_DUMP_CUSTOM_OPTIONS</a> structure that specifies custom minidump options. If this parameter is <b>NULL</b>, the standard minidump information is collected.

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

<a href="/windows/desktop/Debug/minidump-files">Minidump Files</a>



<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/ns-werapi-wer_dump_custom_options">WER_DUMP_CUSTOM_OPTIONS</a>



<a href="/windows/desktop/api/werapi/ns-werapi-wer_exception_information">WER_EXCEPTION_INFORMATION</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werreportcreate">WerReportCreate</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>