---
UID: NF:rpcnsi.RpcNsProfileEltRemoveA
title: RpcNsProfileEltRemoveA function (rpcnsi.h)
description: The RpcNsProfileEltRemove function removes an element from a profile. (ANSI)
helpviewer_keywords: ["RpcNsProfileEltRemoveA", "rpcnsi/RpcNsProfileEltRemoveA"]
old-location: rpc\rpcnsprofileeltremove.htm
tech.root: Rpc
ms.assetid: 303df924-73ad-4e2f-aa30-e600bb5594c2
ms.date: 12/05/2018
ms.keywords: RpcNsProfileEltRemove, RpcNsProfileEltRemove function [RPC], RpcNsProfileEltRemoveA, RpcNsProfileEltRemoveW, _rpc_rpcnsprofileeltremove, rpc.rpcnsprofileeltremove, rpcnsi/RpcNsProfileEltRemove, rpcnsi/RpcNsProfileEltRemoveA, rpcnsi/RpcNsProfileEltRemoveW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsProfileEltRemoveW (Unicode) and RpcNsProfileEltRemoveA (ANSI)
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
 - RpcNsProfileEltRemoveA
 - rpcnsi/RpcNsProfileEltRemoveA
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
 - RpcNsProfileEltRemove
 - RpcNsProfileEltRemoveA
 - RpcNsProfileEltRemoveW
---

# RpcNsProfileEltRemoveA function


## -description

The 
<b>RpcNsProfileEltRemove</b> function removes an element from a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ProfileNameSyntax

Syntax of <i>ProfileName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param ProfileName

Pointer to the name of the profile from which to remove an element.

### -param IfId

Pointer to the interface identification of the profile element to be removed. 




Specify a null value to remove the default profile member.

### -param MemberNameSyntax

Syntax of <i>MemberName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param MemberName

Pointer to the name service–entry name in the profile element to remove.

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
<b>RpcNsProfileEltRemove</b> function removes a profile element from the profile attribute in the <i>ProfileName</i> entry. This function requires an exact match of the <i>MemberName</i> and <i>IfId</i> parameters to remove a profile element. The entry (<i>MemberName</i>), included as a member in the profile element, is not deleted.

<div class="alert"><b>Note</b>  Use 
<b>RpcNsProfileEltRemove</b> cautiously: removing elements from a profile can have the unwanted effect of breaking a hierarchy of profiles.</div>
<div> </div>
<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsProfileEltRemove as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofiledeletea">RpcNsProfileDelete</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltadda">RpcNsProfileEltAdd</a>
