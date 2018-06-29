---
UID: NF:rpcnsi.RpcNsGroupMbrInqNextW
title: RpcNsGroupMbrInqNextW function
author: windows-sdk-content
description: The RpcNsGroupMbrInqNext function returns one entry name from a group at a time.
old-location: rpc\rpcnsgroupmbrinqnext.htm
old-project: Rpc
ms.assetid: 58f32594-85de-4d20-86b2-210367ccb7ce
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcNsGroupMbrInqNext, RpcNsGroupMbrInqNext function [RPC], RpcNsGroupMbrInqNextA, RpcNsGroupMbrInqNextW, _rpc_rpcnsgroupmbrinqnext, rpc.rpcnsgroupmbrinqnext, rpcnsi/RpcNsGroupMbrInqNext, rpcnsi/RpcNsGroupMbrInqNextA, rpcnsi/RpcNsGroupMbrInqNextW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
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
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: ADAM
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
<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a> function. 




Specify a null value to prevent 
<b>RpcNsGroupMbrInqNext</b> from returning the <i>MemberName</i> parameter. In this case, the application does not call the 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupMbrInqNext</b> function returns one member of the RPC group specified by the <i>GroupName</i> parameter in 
<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a>. An application can view all the members of an RPC group set by repeatedly calling 
<b>RpcNsGroupMbrInqNext</b>. When all the group members have been viewed, this function returns an RPC_S_NO_MORE_MEMBERS status code. The returned group members are unordered.

On each call to 
<b>RpcNsGroupMbrInqNext</b> that returns a member name, the RPC run-time library allocates memory for the returned <i>MemberName</i>. The application is responsible for calling 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> for each returned <i>MemberName</i> string. After viewing the RPC group's members, the application must call 
<a href="https://msdn.microsoft.com/fe40be4d-1468-429a-aa20-694467076bde">RpcNsGroupMbrInqDone</a> to release the inquiry context.

The order in which group members are returned can be different for each viewing of a group. This means that the order in which group members are returned to an application can be different each time the application is run.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a>



<a href="https://msdn.microsoft.com/fe40be4d-1468-429a-aa20-694467076bde">RpcNsGroupMbrInqDone</a>



<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>
 

 

