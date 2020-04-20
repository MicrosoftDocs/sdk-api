---
UID: NF:rpcnsi.RpcNsProfileEltInqNextA
title: RpcNsProfileEltInqNextA function (rpcnsi.h)
description: The RpcNsProfileEltInqNext function returns one element at a time from a profile.helpviewer_keywords: ["RpcNsProfileEltInqNext","RpcNsProfileEltInqNext function [RPC]","RpcNsProfileEltInqNextA","RpcNsProfileEltInqNextW","_rpc_rpcnsprofileeltinqnext","rpc.rpcnsprofileeltinqnext","rpcnsi/RpcNsProfileEltInqNext","rpcnsi/RpcNsProfileEltInqNextA","rpcnsi/RpcNsProfileEltInqNextW"]
old-location: rpc\rpcnsprofileeltinqnext.htm
tech.root: Rpc
ms.assetid: 78835fde-82c3-4cff-94b9-91e07120e03f
ms.date: 12/05/2018
ms.keywords: RpcNsProfileEltInqNext, RpcNsProfileEltInqNext function [RPC], RpcNsProfileEltInqNextA, RpcNsProfileEltInqNextW, _rpc_rpcnsprofileeltinqnext, rpc.rpcnsprofileeltinqnext, rpcnsi/RpcNsProfileEltInqNext, rpcnsi/RpcNsProfileEltInqNextA, rpcnsi/RpcNsProfileEltInqNextW
f1_keywords:
- rpcnsi/RpcNsProfileEltInqNext
dev_langs:
- c++
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcNsProfileEltInqNextW (Unicode) and RpcNsProfileEltInqNextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Rpcns4.dll
api_name:
- RpcNsProfileEltInqNext
- RpcNsProfileEltInqNextA
- RpcNsProfileEltInqNextW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcNsProfileEltInqNextA function


## -description


The 
<b>RpcNsProfileEltInqNext</b> function returns one element at a time from a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Name-service handle returned from the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a> function.


### -param IfId

Returns a pointer to the interface identification of the profile element.


### -param MemberName

Returns a pointer to a pointer to the profile element's member name.The syntax of the returned name was specified by the <i>MemberNameSyntax</i> parameter in the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a> function. 




Specify a null value to prevent 
<b>RpcNsProfileEltInqNext</b> from returning the <i>MemberName</i> parameter. In this case, the application does not call the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.


### -param Priority

Returns a pointer to the profile-element priority.


### -param Annotation

Returns a pointer to a pointer to the annotation string for the profile element. If there is no annotation string in the profile element, the string \0 is returned. 




Specify a null value to prevent 
<b>RpcNsProfileEltInqNext</b> from returning the <i>Annotation</i> parameter. In this case, the application does not need to call the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.


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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_MORE_ELEMENTS</b></dt>
</dl>
</td>
<td width="60%">
No more elements.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsProfileEltInqNext</b> function returns one element from the profile specified by the <i>ProfileName</i> parameter in 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a>. Regardless of the value of <i>InquiryType</i> in 
<b>RpcNsProfileEltInqBegin</b>, 
<b>RpcNsProfileEltInqNext</b> returns all the components (interface identification, member name, priority, annotation string) of a profile element.

An application can view all the selected profile entries by repeatedly calling the 
<b>RpcNsProfileEltInqNext</b> function. When all the elements have been viewed, this function returns a RPC_S_NO_MORE_ELEMENTS status code. The returned elements are unordered.

On each call to 
<b>RpcNsProfileEltInqNext</b> that returns a profile element, the RPC run-time library allocates memory for the returned member name and annotation string. The application is responsible for calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function for each returned member name and annotation string. After viewing the profile's elements, the application must call 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqdone">RpcNsProfileEltInqDone</a> to release the inquiry context.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqdone">RpcNsProfileEltInqDone</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
 

 

