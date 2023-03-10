---
UID: NF:tdh.TdhOpenDecodingHandle
title: TdhOpenDecodingHandle function (tdh.h)
description: Opens a decoding handle.
helpviewer_keywords: ["TdhOpenDecodingHandle","TdhOpenDecodingHandle function [ETW]","etw.tdhopendecodinghandle","tdh/TdhOpenDecodingHandle"]
old-location: etw\tdhopendecodinghandle.htm
tech.root: ETW
ms.assetid: ea437d31-a688-4602-8453-f891e83af9ea
ms.date: 12/05/2018
ms.keywords: TdhOpenDecodingHandle, TdhOpenDecodingHandle function [ETW], etw.tdhopendecodinghandle, tdh/TdhOpenDecodingHandle
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - TdhOpenDecodingHandle
 - tdh/TdhOpenDecodingHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhOpenDecodingHandle
---

# TdhOpenDecodingHandle function


## -description

Opens a decoding handle.

## -parameters

### -param Handle [out]

Type: <b>PTDH_HANDLE</b>

A valid decoding handle.

## -returns

Type: <b>ULONG</b>

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. This error is returned if the <i>Handle</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocations failed.

</td>
</tr>
</table>

## -remarks

Call <a href="/windows/desktop/api/tdh/nf-tdh-tdhclosedecodinghandle">TdhCloseDecodingHandle</a> to free the returned handle.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhclosedecodinghandle">TdhCloseDecodingHandle</a>