---
UID: NF:werapi.WerReportAddDump
title: WerReportAddDump function (werapi.h)
description: Adds a dump of the specified type to the specified Windows Error Reporting (WER) report.
helpviewer_keywords: ["WER_DUMP_NOHEAP_ONQUEUE","WerDumpTypeHeapDump","WerDumpTypeMicroDump","WerDumpTypeMiniDump","WerReportAddDump","WerReportAddDump function [Windows Error Reporting]","base.werreportadddump","wer.werreportadddump","werapi/WerReportAddDump"]
old-location: wer\werreportadddump.htm
tech.root: wer
ms.assetid: b40dac44-f7c5-43f0-876d-6f97c26bf461
ms.date: 07/25/2023
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
 - ext-ms-win-wer-reporting-l1-1-3.dll
 - ext-ms-win-wer-reporting-l1-1-2.dll
 - Wer.dll
 - Ext-MS-Win-wer-reporting-l1-1-0.dll
 - errorhandlingext.dll
 - Ext-MS-Win-Wer-Reporting-L1-1-1.dll
api_name:
 - WerReportAddDump
---

# WerReportAddDump function

## -description

Adds a dump of the specified type to the specified [Windows Error Reporting](../_wer/index.md) (WER) report.

## -parameters

### -param hReportHandle [in]

A handle to the report. This handle is returned by the [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate) function.

### -param hProcess [in]

A handle to the process for which the report is being generated. This handle must have the STANDARD_RIGHTS_READ and PROCESS_QUERY_INFORMATION access rights.

### -param hThread [in, optional]

A handle to the thread of *hProcess* for which the report is being generated. If *dumpType* is WerDumpTypeMicro, this parameter is required. For other dump types, this parameter may be **NULL**.

### -param dumpType [in]

The type of [minidump](/windows/desktop/Debug/minidump-files). This parameter can be one of the following values from the **WER_DUMP_TYPE** enumeration type.

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

A pointer to a [WER_EXCEPTION_INFORMATION](/windows/desktop/api/werapi/ns-werapi-wer_exception_information) structure that specifies exception information.

### -param pDumpCustomOptions [in, optional]

A pointer to a [WER_DUMP_CUSTOM_OPTIONS](/windows/desktop/api/werapi/ns-werapi-wer_dump_custom_options) structure that specifies custom minidump options. If this parameter is **NULL**, the standard minidump information is collected.

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

This function returns **S_OK** on success or an error code on failure.

## -remarks

Use this function only for generic reporting—it has no effect on operating system crash or no-response reporting.

If the server asks for a mini dump and you specify **WerDumpTypeHeapDump** for the *dumpType* parameter, WER will not send the heap dump to the Watson server. However, if the server asks for a heap dump and the *dumpType* is **WerDumpTypeMiniDump**, WER will send the mini dump to the server. Thus, it is recommended that you set *dumpType* to **WerDumpTypeMiniDump**.

## -see-also

[Minidump Files](/windows/desktop/Debug/minidump-files), [WER_DUMP_CUSTOM_OPTIONS](/windows/desktop/api/werapi/ns-werapi-wer_dump_custom_options), [WER_EXCEPTION_INFORMATION](/windows/desktop/api/werapi/ns-werapi-wer_exception_information), [WerReportCreate](/windows/desktop/api/werapi/nf-werapi-werreportcreate), [Windows Error Reporting](/windows/desktop/wer)
