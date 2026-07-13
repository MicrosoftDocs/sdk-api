---
UID: NF:rpcnsi.RpcNsProfileEltAddA
title: RpcNsProfileEltAddA function (rpcnsi.h)
description: The RpcNsProfileEltAdd function adds an element to a profile. If necessary, it creates the entry. (ANSI)
helpviewer_keywords: ["RpcNsProfileEltAddA", "rpcnsi/RpcNsProfileEltAddA"]
old-location: rpc\rpcnsprofileeltadd.htm
tech.root: Rpc
ms.assetid: e0a2d4b9-853c-4578-8a15-e0be7bfc0b9b
ms.date: 12/05/2018
ms.keywords: RpcNsProfileEltAdd, RpcNsProfileEltAdd function [RPC], RpcNsProfileEltAddA, RpcNsProfileEltAddW, _rpc_rpcnsprofileeltadd, rpc.rpcnsprofileeltadd, rpcnsi/RpcNsProfileEltAdd, rpcnsi/RpcNsProfileEltAddA, rpcnsi/RpcNsProfileEltAddW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsProfileEltAddW (Unicode) and RpcNsProfileEltAddA (ANSI)
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
 - RpcNsProfileEltAddA
 - rpcnsi/RpcNsProfileEltAddA
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
 - RpcNsProfileEltAdd
 - RpcNsProfileEltAddA
 - RpcNsProfileEltAddW
---

# RpcNsProfileEltAddA function


## -description

The 
<b>RpcNsProfileEltAdd</b> function adds an element to a profile. If necessary, it creates the entry.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ProfileNameSyntax

Syntax of <i>ProfileName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param ProfileName

Pointer to the name of the profile to receive a new element.

### -param IfId

Pointer to the interface identification of the new profile element. To add or replace the default profile element, specify a null value.

### -param MemberNameSyntax

Syntax of <i>MemberName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param MemberName

Pointer to a name service–entry name to include in the new profile element.

### -param Priority

Integer value (0 through 7) that indicates the relative priority for using the new profile element during the import and lookup operations. A value of 0 is the highest priority; a value of 7 is the lowest priority. When adding a default profile member, use a value of 0.

### -param Annotation

Pointer to an annotation string stored as part of the new profile element. Specify a null value or a null-terminated string if there is no annotation string. 




The string is used by applications for informational purposes only. For example, an application can use this string to store the interface-name string specified in the IDL file. RPC does not use the annotation string during lookup or import operations or for enumerating profile elements.

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
<b>RpcNsProfileEltAdd</b> function adds an element to the profile attribute of the name-service entry specified by <i>ProfileName</i>. If the <i>ProfileName</i> entry does not exist, 
<b>RpcNsProfileEltAdd</b> tries to create the entry with a profile attribute and adds the profile element specified by the <i>IfId</i>, <i>MemberName</i>, <i>Priority</i>, and <i>Annotation</i> parameters. In this case, the application must have the privilege to create the entry. Otherwise, a management application with the necessary privileges should create the entry by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentrycreatea">RpcNsMgmtEntryCreate</a> function before the application is run.

If an element with the specified member name and interface identification is already in the profile, 
<b>RpcNsProfileEltAdd</b> updates the element's priority and annotation string using the values provided in the <i>Priority</i> and <i>Annotation</i> parameters.

<div class="alert"><b>Note</b>  The Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsProfileEltAdd as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifinqid">RpcIfInqId</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtentrycreatea">RpcNsMgmtEntryCreate</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltremovea">RpcNsProfileEltRemove</a>
