---
UID: NF:rpcnsi.RpcNsGroupMbrInqBeginA
title: RpcNsGroupMbrInqBeginA function (rpcnsi.h)
description: The RpcNsGroupMbrInqBegin function creates an inquiry context for viewing group members. (ANSI)
helpviewer_keywords: ["RpcNsGroupMbrInqBeginA", "rpcnsi/RpcNsGroupMbrInqBeginA"]
old-location: rpc\rpcnsgroupmbrinqbegin.htm
tech.root: Rpc
ms.assetid: f3a98563-0c7f-4f4b-b272-af7c0366b95d
ms.date: 12/05/2018
ms.keywords: RpcNsGroupMbrInqBegin, RpcNsGroupMbrInqBegin function [RPC], RpcNsGroupMbrInqBeginA, RpcNsGroupMbrInqBeginW, _rpc_rpcnsgroupmbrinqbegin, rpc.rpcnsgroupmbrinqbegin, rpcnsi/RpcNsGroupMbrInqBegin, rpcnsi/RpcNsGroupMbrInqBeginA, rpcnsi/RpcNsGroupMbrInqBeginW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsGroupMbrInqBeginW (Unicode) and RpcNsGroupMbrInqBeginA (ANSI)
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
 - RpcNsGroupMbrInqBeginA
 - rpcnsi/RpcNsGroupMbrInqBeginA
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
 - RpcNsGroupMbrInqBegin
 - RpcNsGroupMbrInqBeginA
 - RpcNsGroupMbrInqBeginW
---

# RpcNsGroupMbrInqBeginA function


## -description

The 
<b>RpcNsGroupMbrInqBegin</b> function creates an inquiry context for viewing group members.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param GroupNameSyntax

Syntax of <i>GroupName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param GroupName

Pointer to the name of the RPC group to view.

### -param MemberNameSyntax

Syntax of the return parameter, <i>MemberName</i>, in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a> function. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param InquiryContext

Returns a pointer to a name-service handle for use with the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a> and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqdone">RpcNsGroupMbrInqDone</a> functions.

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
<dt><b>RPC_S_INVALID_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_NAME_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The name syntax is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INCOMPLETE_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ENTRY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The name-service entry was not found.

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
<b>RpcNsGroupMbrInqBegin</b> function creates an inquiry context for viewing the members of an RPC group. Before calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a>, the application must first call 
<b>RpcNsGroupMbrInqBegin</b> to create an inquiry context. When finished viewing the RPC group members, the application calls 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqdone">RpcNsGroupMbrInqDone</a> to delete the inquiry context.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsGroupMbrInqBegin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbradda">RpcNsGroupMbrAdd</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqdone">RpcNsGroupMbrInqDone</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsgroupmbrinqnexta">RpcNsGroupMbrInqNext</a>
