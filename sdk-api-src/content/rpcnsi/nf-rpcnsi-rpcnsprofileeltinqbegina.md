---
UID: NF:rpcnsi.RpcNsProfileEltInqBeginA
title: RpcNsProfileEltInqBeginA function (rpcnsi.h)
description: The RpcNsProfileEltInqBegin function creates an inquiry context for viewing the elements in a profile. (ANSI)
helpviewer_keywords: ["RPC_C_PROFILE_ALL_ELTS", "RPC_C_PROFILE_DEFAULT_ELT", "RPC_C_PROFILE_MATCH_BY_BOTH", "RPC_C_PROFILE_MATCH_BY_IF", "RPC_C_PROFILE_MATCH_BY_MBR", "RPC_C_VERS_ALL", "RPC_C_VERS_COMPATIBLE", "RPC_C_VERS_EXACT", "RPC_C_VERS_MAJOR_ONLY", "RPC_C_VERS_UPTO", "RpcNsProfileEltInqBeginA", "rpcnsi/RpcNsProfileEltInqBeginA"]
old-location: rpc\rpcnsprofileeltinqbegin.htm
tech.root: Rpc
ms.assetid: 5b14eb21-0c3e-4f12-b1dc-95b364d87a4f
ms.date: 12/05/2018
ms.keywords: RPC_C_PROFILE_ALL_ELTS, RPC_C_PROFILE_DEFAULT_ELT, RPC_C_PROFILE_MATCH_BY_BOTH, RPC_C_PROFILE_MATCH_BY_IF, RPC_C_PROFILE_MATCH_BY_MBR, RPC_C_VERS_ALL, RPC_C_VERS_COMPATIBLE, RPC_C_VERS_EXACT, RPC_C_VERS_MAJOR_ONLY, RPC_C_VERS_UPTO, RpcNsProfileEltInqBegin, RpcNsProfileEltInqBegin function [RPC], RpcNsProfileEltInqBeginA, RpcNsProfileEltInqBeginW, _rpc_rpcnsprofileeltinqbegin, rpc.rpcnsprofileeltinqbegin, rpcnsi/RpcNsProfileEltInqBegin, rpcnsi/RpcNsProfileEltInqBeginA, rpcnsi/RpcNsProfileEltInqBeginW
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsProfileEltInqBeginW (Unicode) and RpcNsProfileEltInqBeginA (ANSI)
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
 - RpcNsProfileEltInqBeginA
 - rpcnsi/RpcNsProfileEltInqBeginA
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
 - RpcNsProfileEltInqBegin
 - RpcNsProfileEltInqBeginA
 - RpcNsProfileEltInqBeginW
---

# RpcNsProfileEltInqBeginA function


## -description

The 
<b>RpcNsProfileEltInqBegin</b> function creates an inquiry context for viewing the elements in a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ProfileNameSyntax

Syntax of <i>ProfileName</i>. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param ProfileName

Pointer to the name of the profile to view.

### -param InquiryType

Type of inquiry to perform on the profile. The following table lists valid inquiry types. 



<table>
<tr>
<th>Inquiry type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_PROFILE_DEFAULT_ELT"></a><a id="rpc_c_profile_default_elt"></a><dl>
<dt><b>RPC_C_PROFILE_DEFAULT_ELT</b></dt>
</dl>
</td>
<td width="60%">
Searches the profile for the default profile element, if any. The <i>IfId</i>, <i>VersOption</i>, and <i>MemberName</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_PROFILE_ALL_ELTS"></a><a id="rpc_c_profile_all_elts"></a><dl>
<dt><b>RPC_C_PROFILE_ALL_ELTS</b></dt>
</dl>
</td>
<td width="60%">
Returns every element from the profile. The <i>IfId</i>, <i>VersOption</i>, and <i>MemberName</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_PROFILE_MATCH_BY_IF"></a><a id="rpc_c_profile_match_by_if"></a><dl>
<dt><b>RPC_C_PROFILE_MATCH_BY_IF</b></dt>
</dl>
</td>
<td width="60%">
Searches the profile for elements that contain the interface identification specified by <i>IfId</i> and <i>VersOption</i>. The <i>MemberName</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_PROFILE_MATCH_BY_MBR"></a><a id="rpc_c_profile_match_by_mbr"></a><dl>
<dt><b>RPC_C_PROFILE_MATCH_BY_MBR</b></dt>
</dl>
</td>
<td width="60%">
Searches the profile for elements that contain <i>MemberName</i>. The <i>IfId</i> and <i>VersOption</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_PROFILE_MATCH_BY_BOTH"></a><a id="rpc_c_profile_match_by_both"></a><dl>
<dt><b>RPC_C_PROFILE_MATCH_BY_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Searches the profile for elements that contain the interface identification and member identified by the <i>IfId</i>, <i>VersOption</i>, and <i>MemberName</i> parameters.

</td>
</tr>
</table>

### -param IfId

Pointer to the interface identification of the profile elements to be returned by the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function. 




The <i>IfId</i> parameter is used only when specifying a value of RPC_C_PROFILE_MATCH_BY_IF or RPC_C_PROFILE_MATCH_BY_BOTH for the <i>InquiryType</i> parameter. Otherwise, <i>IfId</i> is ignored and a null value can be specified.

### -param VersOption

Specifies how the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function uses the <i>IfId</i> parameter. This parameter is used only when specifying a value of RPC_C_PROFILE_MATCH_BY_IF or RPC_C_PROFILE_MATCH_BY_BOTH for <i>InquiryType</i>. Otherwise, this parameter is ignored and a 0 value can be specified. 




The following table describes valid values for <i>VersOption</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_ALL"></a><a id="rpc_c_vers_all"></a><dl>
<dt><b>RPC_C_VERS_ALL</b></dt>
</dl>
</td>
<td width="60%">
Returns profile elements that offer the specified interface UUID, regardless of the version numbers. For this value, specify 0 for both the major and minor versions in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_COMPATIBLE"></a><a id="rpc_c_vers_compatible"></a><dl>
<dt><b>RPC_C_VERS_COMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
Returns profile elements that offer the same major version of the specified interface UUID and a minor version greater than or equal to the minor version of the specified interface UUID.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_EXACT"></a><a id="rpc_c_vers_exact"></a><dl>
<dt><b>RPC_C_VERS_EXACT</b></dt>
</dl>
</td>
<td width="60%">
Returns profile elements that offer the specified version of the specified interface UUID.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_MAJOR_ONLY"></a><a id="rpc_c_vers_major_only"></a><dl>
<dt><b>RPC_C_VERS_MAJOR_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Returns profile elements that offer the same major version of the specified interface UUID (ignores the minor version). For this value, specify 0 for the minor version in <i>IfId</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_UPTO"></a><a id="rpc_c_vers_upto"></a><dl>
<dt><b>RPC_C_VERS_UPTO</b></dt>
</dl>
</td>
<td width="60%">
Returns profile elements that offer a version of the specified interface UUID less than or equal to the specified major and minor version. (For example, if the <i>IfId</i> contained V2.0 and the profile contained elements with V1.3, V2.0, and V2.1, the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function returns elements with V1.3 and V2.0.)

</td>
</tr>
</table>

### -param MemberNameSyntax

Syntax of <i>MemberName</i>, and the return parameter <i>MemberName</i> in the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.

### -param MemberName

Pointer to the member name that the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function looks for in profile elements. The <i>MemberName</i> parameter is used only when specifying a value of RPC_C_PROFILE_MATCH_BY_MBR or RPC_C_PROFILE_MATCH_BY_BOTH for <i>InquiryType</i>. Otherwise, <i>MemberName</i> is ignored and a null value can be specified.

### -param InquiryContext

Returns a pointer to a name-service handle for use with the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> and 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqdone">RpcNsProfileEltInqDone</a> functions.

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
<dt><b>RPC_S_INVALID_VERS_OPTION</b></dt>
</dl>
</td>
<td width="60%">
The version option is invalid.

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
<b>RpcNsProfileEltInqBegin</b> function creates an inquiry context for viewing the elements in a profile.

Using the <i>InquiryType</i> parameter, an application specifies which of the following profile elements are to be returned from calls to 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a>:

<ul>
<li>The default element</li>
<li>All elements</li>
<li>Elements with the specified interface identification</li>
<li>Elements with the specified member name</li>
<li>Elements with both the specified interface identification and member name</li>
</ul>
Before calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a>, the application must first call 
<b>RpcNsProfileEltInqBegin</b> to create an inquiry context.

When finished viewing the profile elements, the application calls the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqdone">RpcNsProfileEltInqDone</a> function to delete the inquiry context.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>




> [!NOTE]
> The rpcnsi.h header defines RpcNsProfileEltInqBegin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifinqid">RpcIfInqId</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqdone">RpcNsProfileEltInqDone</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a>
