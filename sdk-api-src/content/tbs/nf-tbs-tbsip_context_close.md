---
UID: NF:tbs.Tbsip_Context_Close
title: Tbsip_Context_Close function (tbs.h)
description: Closes a context handle, which releases resources associated with the context in TBS and closes the binding handle used to communicate with TBS.
helpviewer_keywords: ["Tbsip_Context_Close","Tbsip_Context_Close function [TBS]","tbs._tbsip_context_close","tbs/Tbsip_Context_Close"]
old-location: tbs\_tbsip_context_close.htm
tech.root: TBS
ms.assetid: 405c600b-f752-48e8-9eea-473fcdf1eb2f
ms.date: 12/05/2018
ms.keywords: Tbsip_Context_Close, Tbsip_Context_Close function [TBS], tbs._tbsip_context_close, tbs/Tbsip_Context_Close
req.header: tbs.h
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
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsip_Context_Close
 - tbs/Tbsip_Context_Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsip_Context_Close
---

# Tbsip_Context_Close function


## -description

Closes a context handle, which releases resources associated with the context in TBS and closes the binding handle used to communicate with TBS.

## -parameters

### -param hContext [in]

A handle of the context to be closed.

## -returns

If the function succeeds, the function returns TBS_SUCCESS.

If the function fails, it returns a TBS return code that indicates the error.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INTERNAL_ERROR</b></dt>
<dt>2150121473 (0x80284001)</dt>
</dl>
</td>
<td width="60%">
An internal software error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_INVALID_CONTEXT</b></dt>
<dt>2150121476 (0x80284004)</dt>
</dl>
</td>
<td width="60%">
The specified context handle does not refer to a valid context.

</td>
</tr>
</table>

## -remarks

When the context handle is closed, the structure associated with the context handle is zeroed, which ensures that  subsequent attempts to use the handle will result in an error. All objects that have been created under this context will be flushed.

