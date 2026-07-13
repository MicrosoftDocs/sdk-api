---
UID: NF:tdh.TdhLoadManifest
title: TdhLoadManifest function (tdh.h)
description: Loads the manifest used to decode a log file.
helpviewer_keywords: ["TdhLoadManifest","TdhLoadManifest function [ETW]","etw.tdhloadmanifest","tdh/TdhLoadManifest"]
old-location: etw\tdhloadmanifest.htm
tech.root: ETW
ms.assetid: 85dfcf73-ea3a-47e2-ad1a-3891b3917ecf
ms.date: 12/05/2018
ms.keywords: TdhLoadManifest, TdhLoadManifest function [ETW], etw.tdhloadmanifest, tdh/TdhLoadManifest
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhLoadManifest
 - tdh/TdhLoadManifest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhLoadManifest
---

# TdhLoadManifest function


## -description

Loads the manifest used to decode a log file.

## -parameters

### -param Manifest [in]

The full path to the manifest.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The manifest file was not found at the specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Manifest</i> parameter cannot be <b>NULL</b> and the path cannot exceed MAX_PATH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_XML_PARSE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The manifest did not pass validation. To determine the validation errors, run the manifest through the message compiler (mc.exe).

</td>
</tr>
</table>

## -remarks

To consume events, TDH requires the provider's manifest. Typically, you decode the log file on a computer that contains the provider. Since the provider includes the manifest as a resource, TDH uses the provider to get the manifest. To decode the log file on a computer that does not contain the provider, you must first use the  TraceRpt.exe executable to export the manifest (see the –export switch) from the provider on a computer that does contain the provider. After you have the manifest file, you can decode the log file on a computer that does not contain the provider.

You need to call this function before decoding the first event. For example, you can call this function before calling the <a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function. After processing all the events, call the <a href="/windows/desktop/api/tdh/nf-tdh-tdhunloadmanifest">TdhUnloadManifest</a> function.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhunloadmanifest">TdhUnloadManifest</a>