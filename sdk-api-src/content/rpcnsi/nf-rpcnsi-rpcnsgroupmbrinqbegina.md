---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a> function. 




To use the syntax specified in the registry value entry <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\NameService\DefaultSyntax</b>, provide a value of RPC_C_NS_SYNTAX_DEFAULT.


### -param InquiryContext

Returns a pointer to a name-service handle for use with the 
<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a> and 
<a href="https://msdn.microsoft.com/fe40be4d-1468-429a-aa20-694467076bde">RpcNsGroupMbrInqDone</a> functions.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupMbrInqBegin</b> function creates an inquiry context for viewing the members of an RPC group. Before calling 
<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a>, the application must first call 
<b>RpcNsGroupMbrInqBegin</b> to create an inquiry context. When finished viewing the RPC group members, the application calls 
<a href="https://msdn.microsoft.com/fe40be4d-1468-429a-aa20-694467076bde">RpcNsGroupMbrInqDone</a> to delete the inquiry context.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fa32b5e5-1a8a-44f4-aa38-81b024f4db51">RpcNsGroupMbrAdd</a>



<a href="https://msdn.microsoft.com/fe40be4d-1468-429a-aa20-694467076bde">RpcNsGroupMbrInqDone</a>



<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a>
 

 

