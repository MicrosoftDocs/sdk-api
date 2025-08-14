---
UID: NF:tdh.TdhUnloadManifest
title: TdhUnloadManifest function (tdh.h)
description: Unloads the manifest that was loaded by the TdhLoadManifest function.
helpviewer_keywords: ["TdhUnloadManifest","TdhUnloadManifest function [ETW]","etw.tdhunloadmanifest","tdh/TdhUnloadManifest"]
old-location: etw\tdhunloadmanifest.htm
tech.root: ETW
ms.assetid: ce0dd781-04b2-4e0c-9e79-44864f53f176
ms.date: 12/05/2018
ms.keywords: TdhUnloadManifest, TdhUnloadManifest function [ETW], etw.tdhunloadmanifest, tdh/TdhUnloadManifest
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
 - TdhUnloadManifest
 - tdh/TdhUnloadManifest
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
 - TdhUnloadManifest
---

# TdhUnloadManifest function

## -description

Unloads the manifest that was loaded by the <a href="/windows/desktop/api/tdh/nf-tdh-tdhloadmanifest">TdhLoadManifest</a> function.

## -parameters

### -param Manifest [in]

The full path to the loaded manifest.

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

You must call this function after processing all the events. For example, you can call this function after calling <a href="/windows/desktop/ETW/closetrace">CloseTrace</a>.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhloadmanifest">TdhLoadManifest</a>