---
UID: NF:tbs.Tbsip_Cancel_Commands
title: Tbsip_Cancel_Commands function (tbs.h)
description: Cancels all outstanding commands for the specified context.
helpviewer_keywords: ["Tbsip_Cancel_Commands","Tbsip_Cancel_Commands function [TBS]","tbs._tbsip_cancel_commands","tbs/Tbsip_Cancel_Commands"]
old-location: tbs\_tbsip_cancel_commands.htm
tech.root: TBS
ms.assetid: aaf209cb-2250-4c23-900f-9026d2f44e24
ms.date: 12/05/2018
ms.keywords: Tbsip_Cancel_Commands, Tbsip_Cancel_Commands function [TBS], tbs._tbsip_cancel_commands, tbs/Tbsip_Cancel_Commands
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
 - Tbsip_Cancel_Commands
 - tbs/Tbsip_Cancel_Commands
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
 - Tbsip_Cancel_Commands
---

# Tbsip_Cancel_Commands function


## -description

Cancels all outstanding commands for the specified context.

## -parameters

### -param hContext [in]

A TBS handle to the context whose commands are to be canceled and that was obtained from previous call to the <a href="/windows/desktop/api/tbs/nf-tbs-tbsi_context_create">Tbsi_Context_Create</a> function.

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
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_IOERROR</b></dt>
<dt>2150121478 (0x80284006)</dt>
</dl>
</td>
<td width="60%">
An error occurred while communicating with the TPM.

</td>
</tr>
</table>

## -remarks

When a command is canceled, TBS sends a message to the command that indicates that the command was canceled.