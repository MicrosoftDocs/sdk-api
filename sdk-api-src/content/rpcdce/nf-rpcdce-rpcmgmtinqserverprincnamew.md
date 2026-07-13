---
UID: NF:rpcdce.RpcMgmtInqServerPrincNameW
title: RpcMgmtInqServerPrincNameW function (rpcdce.h)
description: The RpcMgmtInqServerPrincNameW (Unicode) function (rpcdce.h) returns a server's principal name.
helpviewer_keywords: ["RpcMgmtInqServerPrincName", "RpcMgmtInqServerPrincName function [RPC]", "RpcMgmtInqServerPrincNameW", "_rpc_rpcmgmtinqserverprincname", "rpc.rpcmgmtinqserverprincname", "rpcdce/RpcMgmtInqServerPrincName", "rpcdce/RpcMgmtInqServerPrincNameW"]
old-location: rpc\rpcmgmtinqserverprincname.htm
tech.root: Rpc
ms.assetid: 2666adb4-8a89-480e-8855-9179a7128e35
ms.date: 08/16/2022
ms.keywords: RpcMgmtInqServerPrincName, RpcMgmtInqServerPrincName function [RPC], RpcMgmtInqServerPrincNameA, RpcMgmtInqServerPrincNameW, _rpc_rpcmgmtinqserverprincname, rpc.rpcmgmtinqserverprincname, rpcdce/RpcMgmtInqServerPrincName, rpcdce/RpcMgmtInqServerPrincNameA, rpcdce/RpcMgmtInqServerPrincNameW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcMgmtInqServerPrincNameW (Unicode) and RpcMgmtInqServerPrincNameA (ANSI)
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
 - RpcMgmtInqServerPrincNameW
 - rpcdce/RpcMgmtInqServerPrincNameW
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
 - RpcMgmtInqServerPrincName
 - RpcMgmtInqServerPrincNameA
 - RpcMgmtInqServerPrincNameW
---

# RpcMgmtInqServerPrincNameW function


## -description

The 
<b>RpcMgmtInqServerPrincName</b> function returns a server's principal name.

## -parameters

### -param Binding

To receive the principal name for a server, specify a server binding handle for that server. To receive the principal name for your own (local) application, specify a value of <b>NULL</b>.

### -param AuthnSvc

Authentication service for which a principal name is returned. Valid values are the constant for any valid security provider.

### -param ServerPrincName

Returns a principal name that is registered for the authentication service in <i>AuthnSvc</i> by the server referenced in <i>Binding</i>. If multiple names are registered, only one name is returned.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>RpcMgmtInqServerPrincName</b> function to obtain the principal name of a server that is registered for a specified authentication service.
			

The RPC run-time library allocates memory for the string returned in <i>ServerPrincName</i>. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function to release the memory used by this function.

The server must be listening for remote procedure calls for this function to succeed.  If the server is not listening, the function fails.





> [!NOTE]
> The rpcdce.h header defines RpcMgmtInqServerPrincName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
