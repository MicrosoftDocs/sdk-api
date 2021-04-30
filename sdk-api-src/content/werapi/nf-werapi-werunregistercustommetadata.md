---
UID: NF:werapi.WerUnregisterCustomMetadata
title: WerUnregisterCustomMetadata function (werapi.h)
description: Removes an item of app-specific metadata being collected during error reporting for the application.
helpviewer_keywords: ["WerUnRegisterCustomMetadata","WerUnRegisterCustomMetadata function [Windows Error Reporting]","WerUnregisterCustomMetadata","wer.werunregistercustommetadata","werapi/WerUnRegisterCustomMetadata"]
old-location: wer\werunregistercustommetadata.htm
tech.root: wer
ms.assetid: 29DB2CE5-2A96-450B-96C8-082B786613F9
ms.date: 12/05/2018
ms.keywords: WerUnRegisterCustomMetadata, WerUnRegisterCustomMetadata function [Windows Error Reporting], WerUnregisterCustomMetadata, wer.werunregistercustommetadata, werapi/WerUnRegisterCustomMetadata
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
 - WerUnregisterCustomMetadata
 - werapi/WerUnregisterCustomMetadata
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
 - WerUnRegisterCustomMetadata
---

# WerUnregisterCustomMetadata function


## -description

Removes an item of app-specific metadata being collected during error reporting for the application.

## -parameters

### -param key

The "key" string for the metadata element being removed. It must have been previously registered with the <a href="/windows/desktop/api/werapi/nf-werapi-werregistercustommetadata">WerRegisterCustomMetadata</a> function.

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
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="/windows/desktop/wsw/portal">application recovery mode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
WER could not find the metadata item to remove.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werregistercustommetadata">WerRegisterCustomMetadata</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>