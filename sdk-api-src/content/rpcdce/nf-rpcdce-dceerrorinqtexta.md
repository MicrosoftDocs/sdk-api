---
UID: NF:rpcdce.DceErrorInqTextA
title: DceErrorInqTextA function (rpcdce.h)
description: The DceErrorInqText function returns the message text for a status code. (DceErrorInqTextA)
helpviewer_keywords: ["DceErrorInqTextA", "RPC_S_INVALID_ARG", "RPC_S_OK", "rpcdce/DceErrorInqTextA"]
old-location: rpc\dceerrorinqtext.htm
tech.root: Rpc
ms.assetid: 0aea211b-48bb-4a2f-a42e-1f35259e7f82
ms.date: 12/05/2018
ms.keywords: DceErrorInqText, DceErrorInqText function [RPC], DceErrorInqTextA, DceErrorInqTextW, RPC_S_INVALID_ARG, RPC_S_OK, _rpc_dceerrorinqtext, rpc.dceerrorinqtext, rpcdce/DceErrorInqText, rpcdce/DceErrorInqTextA, rpcdce/DceErrorInqTextW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DceErrorInqTextW (Unicode) and DceErrorInqTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DceErrorInqTextA
 - rpcdce/DceErrorInqTextA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - DceErrorInqText
 - DceErrorInqTextA
 - DceErrorInqTextW
---

# DceErrorInqTextA function


## -description

The 
<b>DceErrorInqText</b> function returns the message text for a status code.

## -parameters

### -param RpcStatus

Status code to convert to a text string.

### -param ErrorText

Returns the text corresponding to the error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_S_OK"></a><a id="rpc_s_ok"></a><dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_S_INVALID_ARG"></a><a id="rpc_s_invalid_arg"></a><dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
Unknown error code.

</td>
</tr>
</table>

## -returns

This function returns RPC_S_OK if it is successful, or an error code if not.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>DceErrorInqText</b> routine fills the string pointed to by the <i>ErrorText</i> parameter with a null-terminated character string message for a particular status code.




> [!NOTE]
> The rpcdce.h header defines DceErrorInqText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
