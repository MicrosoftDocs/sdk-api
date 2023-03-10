---
UID: NF:tdh.TdhGetDecodingParameter
title: TdhGetDecodingParameter function (tdh.h)
description: Retrieves the value of a decoding parameter.
helpviewer_keywords: ["TdhGetDecodingParameter","TdhGetDecodingParameter function [ETW]","etw.tdhgetdecodingparameter","tdh/TdhGetDecodingParameter"]
old-location: etw\tdhgetdecodingparameter.htm
tech.root: ETW
ms.assetid: 81aeea7c-fd35-4fa8-af72-804006c22f7b
ms.date: 12/05/2018
ms.keywords: TdhGetDecodingParameter, TdhGetDecodingParameter function [ETW], etw.tdhgetdecodingparameter, tdh/TdhGetDecodingParameter
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
 - TdhGetDecodingParameter
 - tdh/TdhGetDecodingParameter
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
 - TdhGetDecodingParameter
---

# TdhGetDecodingParameter function


## -description

Retrieves the value of a decoding parameter.

## -parameters

### -param Handle [in]

Type: <b>TDH_HANDLE</b>

A valid decoding handle.

### -param TdhContext [in, out]

Type: <b><a href="/windows/desktop/api/tdh/ns-tdh-tdh_context">PTDH_CONTEXT</a></b>

Array of context values. The array must not contain duplicate context types.

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
One or more of the parameters is incorrect. This error is returned if the <i>Handle</i> or <i>TdhContext</i>   parameter is <b>NULL</b>. This error is also returned if the <b>ParameterValue</b> member of the <a href="/windows/desktop/api/tdh/ns-tdh-tdh_context">TDH_CONTEXT</a> struct pointed to by the <i>TdhContext</i>   parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
Memory allocations failed.

</td>
</tr>
</table>

## -see-also
<a href="/windows/desktop/api/tdh/ns-tdh-tdh_context">TDH_CONTEXT</a>