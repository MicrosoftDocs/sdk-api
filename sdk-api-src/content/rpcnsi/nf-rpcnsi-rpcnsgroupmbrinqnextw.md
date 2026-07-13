---
UID: NF:rpcnsi.RpcNsGroupMbrInqNextW
title: RpcNsGroupMbrInqNextW function (rpcnsi.h)
description: The RpcNsGroupMbrInqNext function returns one entry name from a group at a time. (Unicode)
helpviewer_keywords: ["RpcNsGroupMbrInqNext", "RpcNsGroupMbrInqNext function [RPC]", "RpcNsGroupMbrInqNextW", "_rpc_rpcnsgroupmbrinqnext", "rpc.rpcnsgroupmbrinqnext", "rpcnsi/RpcNsGroupMbrInqNext", "rpcnsi/RpcNsGroupMbrInqNextW"]
old-location: rpc\rpcnsgroupmbrinqnext.htm
tech.root: Rpc
ms.assetid: 58f32594-85de-4d20-86b2-210367ccb7ce
ms.date: 12/05/2018
ms.keywords: RpcNsGroupMbrInqNext, RpcNsGroupMbrInqNext function [RPC], RpcNsGroupMbrInqNextA, RpcNsGroupMbrInqNextW, _rpc_rpcnsgroupmbrinqnext, rpc.rpcnsgroupmbrinqnext, rpcnsi/RpcNsGroupMbrInqNext, rpcnsi/RpcNsGroupMbrInqNextA, rpcnsi/RpcNsGroupMbrInqNextW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupMbrInqNextW (Unicode) and RpcNsGroupMbrInqNextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsGroupMbrInqNextW
 - rpcnsi/RpcNsGroupMbrInqNextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsGroupMbrInqNext
 - RpcNsGroupMbrInqNextA
 - RpcNsGroupMbrInqNextW
---

# RpcNsGroupMbrInqNextW function


## -description

The 
<b>RpcNsGroupMbrInqNext</b> function returns one entry name from a group at a time.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param InquiryContext

Name service handle.

### -param MemberName

Returns the address of a pointer to an RPC group member name. The syntax of the returned name was specified by the <i>MemberNameSyntax</i> parameter in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqbegina">RpcNsGroupMbrInqBegin</a> function. 




Specify a null value to prevent 
<b>RpcNsGroupMbrInqNext</b> from returning the <i>MemberName</i> parameter. In this case, the application does not call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.

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
<dt><b>RPC_S_INVALID_NS_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The name-service handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_MORE_MEMBERS</b></dt>
</dl>
</td>
<td width="60%">
No more members.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsGroupMbrInqNext</b> function returns one member of the RPC group specified by the <i>GroupName</i> parameter in 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqbegina">RpcNsGroupMbrInqBegin</a>. An application can view all the members of an RPC group set by repeatedly calling 
<b>RpcNsGroupMbrInqNext</b>. When all the group members have been viewed, this function returns an RPC_S_NO_MORE_MEMBERS status code. The returned group members are unordered.

On each call to 
<b>RpcNsGroupMbrInqNext</b> that returns a member name, the RPC run-time library allocates memory for the returned <i>MemberName</i>. The application is responsible for calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> for each returned <i>MemberName</i> string. After viewing the RPC group's members, the application must call 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqdone">RpcNsGroupMbrInqDone</a> to release the inquiry context.

The order in which group members are returned can be different for each viewing of a group. This means that the order in which group members are returned to an application can be different each time the application is run.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsGroupMbrInqNext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqbegina">RpcNsGroupMbrInqBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqdone">RpcNsGroupMbrInqDone</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
