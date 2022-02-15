---
UID: NF:werapi.WerRegisterCustomMetadata
title: WerRegisterCustomMetadata function (werapi.h)
description: Registers app-specific metadata to be collected (in the form of key/value strings) when WER creates an error report.
helpviewer_keywords: ["WerRegisterCustomMetadata","WerRegisterCustomMetadata function [Windows Error Reporting]","wer.werregistercustommetadata","werapi/WerRegisterCustomMetadata"]
old-location: wer\werregistercustommetadata.htm
tech.root: wer
ms.assetid: 55FB3110-314A-4327-AA8F-3AF77B7006DD
ms.date: 12/05/2018
ms.keywords: WerRegisterCustomMetadata, WerRegisterCustomMetadata function [Windows Error Reporting], wer.werregistercustommetadata, werapi/WerRegisterCustomMetadata
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - WerRegisterCustomMetadata
 - werapi/WerRegisterCustomMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerRegisterCustomMetadata
---

# WerRegisterCustomMetadata function


## -description

Registers app-specific metadata to be collected (in the form of key/value strings) when WER creates an error report.

## -parameters

### -param key

The "key" string for the metadata element being registered.

### -param value

The value string for the metadata element being registered.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Strings were <b>NULL</b>, key length was greater than 64 characters or was an invalid xml element name, or <i>value</i> length was greater than 128 characters or contained characters that were not ASCII printable characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
WER could not allocate a large enough heap for the data

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of registered entries (<b>WER_MAX_REGISTERED_ENTRIES</b>) or  maximum amount of registered metadata (<b>WER_MAX_REGISTERED_METADATA</b>) has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="/windows/desktop/wsw/portal">application recovery mode</a>.

</td>
</tr>
</table>

## -remarks

This API allows apps to integrate their own app-level telemetry with system-level telemetry (WER) by associating app metadata with crash reports corresponding to their processes.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werunregistercustommetadata">WerUnregisterCustomMetadata</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>