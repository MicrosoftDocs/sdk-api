---
UID: NF:rpcdce.RpcMgmtEpEltInqBegin
title: RpcMgmtEpEltInqBegin function
author: windows-sdk-content
description: The RpcMgmtEpEltInqBegin function creates an inquiry context for viewing the elements in an endpoint map.
old-location: rpc\rpcmgmtepeltinqbegin.htm
old-project: Rpc
ms.assetid: 659ab657-e17f-46a9-942e-aa2631c1716d
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RPC_C_EP_ALL_ELTS, RPC_C_EP_MATCH_BY_BOTH, RPC_C_EP_MATCH_BY_IF, RPC_C_EP_MATCH_BY_OBJ, RPC_C_VERS_ALL, RPC_C_VERS_COMPATIBLE, RPC_C_VERS_EXACT, RPC_C_VERS_MAJOR_ONLY, RPC_C_VERS_UPTO, RpcMgmtEpEltInqBegin, RpcMgmtEpEltInqBegin function [RPC], _rpc_rpcmgmtepeltinqbegin, rpc.rpcmgmtepeltinqbegin, rpcdce/RpcMgmtEpEltInqBegin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcMgmtEpEltInqBegin
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcMgmtEpEltInqBegin function


## -description


The 
<b>RpcMgmtEpEltInqBegin</b> function creates an inquiry context for viewing the elements in an endpoint map.


## -parameters




### -param EpBinding

Binding handle to a host whose endpoint-map elements is to be viewed. Specify <b>NULL</b> to view elements from the local host. If a binding handle is specified, the object UUID on the binding handle must be <b>NULL</b>. If present, the endpoint on the binding handle is ignored and the endpoint to the endpoint mapper database on the given host is used.


### -param InquiryType

Integer value that indicates the type of inquiry to perform on the endpoint map. The following are valid inquiry types. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_EP_ALL_ELTS"></a><a id="rpc_c_ep_all_elts"></a><dl>
<dt><b>RPC_C_EP_ALL_ELTS</b></dt>
</dl>
</td>
<td width="60%">
Returns every element from the endpoint map. The <i>IfId</i>, <i>VersOption</i>, and <i>ObjectUuid</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_EP_MATCH_BY_IF"></a><a id="rpc_c_ep_match_by_if"></a><dl>
<dt><b>RPC_C_EP_MATCH_BY_IF</b></dt>
</dl>
</td>
<td width="60%">
Searches the endpoint map for elements that contain the interface identifier specified by the <i>IfId</i> and <i>VersOption</i> values.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_EP_MATCH_BY_OBJ"></a><a id="rpc_c_ep_match_by_obj"></a><dl>
<dt><b>RPC_C_EP_MATCH_BY_OBJ</b></dt>
</dl>
</td>
<td width="60%">
Searches the endpoint map for elements that contain the object UUID specified by <i>ObjectUuid</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_EP_MATCH_BY_BOTH"></a><a id="rpc_c_ep_match_by_both"></a><dl>
<dt><b>RPC_C_EP_MATCH_BY_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Searches the endpoint map for elements that contain the interface identifier and object UUID specified by <i>IfId</i>, <i>VersOption</i>, and <i>ObjectUuid</i>.

</td>
</tr>
</table>
 


### -param IfId

Interface identifier of the endpoint-map elements to be returned by 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>. This parameter is only used when <i>InquiryType</i> is either RPC_C_EP_MATCH_BY_IF or RPC_C_EP_MATCH_BY_BOTH. Otherwise, it is ignored.


### -param VersOption

Specifies how 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a> uses the <i>IfId</i> parameter. This parameter is only used when <i>InquiryType</i> is either RPC_C_EP_MATCH_BY_IF or RPC_C_EP_MATCH_BY_BOTH. Otherwise, it is ignored. The following are valid values for this parameter. 



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
Returns endpoint-map elements that offer the specified interface 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>, regardless of the version numbers.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_COMPATIBLE"></a><a id="rpc_c_vers_compatible"></a><dl>
<dt><b>RPC_C_VERS_COMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
Returns endpoint-map elements that offer the same major version of the specified interface 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> and a minor version greater than or equal to the minor version of the specified interface 
<b>UUID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_EXACT"></a><a id="rpc_c_vers_exact"></a><dl>
<dt><b>RPC_C_VERS_EXACT</b></dt>
</dl>
</td>
<td width="60%">
Returns endpoint-map elements that offer the specified version of the specified interface 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_MAJOR_ONLY"></a><a id="rpc_c_vers_major_only"></a><dl>
<dt><b>RPC_C_VERS_MAJOR_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Returns endpoint-map elements that offer the same major version of the specified interface 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> and ignores the minor version.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_VERS_UPTO"></a><a id="rpc_c_vers_upto"></a><dl>
<dt><b>RPC_C_VERS_UPTO</b></dt>
</dl>
</td>
<td width="60%">
Returns endpoint-map elements that offer a version of the specified interface 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> less than or equal to the specified major and minor version.

</td>
</tr>
</table>
 


### -param ObjectUuid

The object UUID that 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a> looks for in endpoint-map elements. This parameter is used only when <i>InquiryType</i> is either RPC_C_EP_MATCH_BY_OBJ or RPC_C_EP_MATCH_BY_BOTH.


### -param InquiryContext

Returns an inquiry context for use with 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a> and 
<a href="https://msdn.microsoft.com/7a0aac99-8829-4720-a388-da88d015d596">RpcMgmtEpEltInqDone</a>. See 
<a href="https://msdn.microsoft.com/e18ce800-0110-4450-9a1b-a3f777d00f2d">RPC_EP_INQ_HANDLE</a>.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcMgmtEpEltInqBegin</b> function creates an inquiry context for viewing server-address information stored in the endpoint map. Using <i>InquiryType</i> and <i>VersOption</i>, an application specifies which of the following endpoint-map elements are to be returned from calls to 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>:

<ul>
<li>All elements</li>
<li>Those elements with the specified interface identifier</li>
<li>Those elements with the specified object UUID</li>
<li>Those elements with both the specified interface identifier and object UUID</li>
</ul>
Before calling 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>, the application must first call this function to create an inquiry context. After viewing the endpoint-map elements, the application calls 
<a href="https://msdn.microsoft.com/7a0aac99-8829-4720-a388-da88d015d596">RpcMgmtEpEltInqDone</a> to delete the inquiry context.




## -see-also




<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/7a0aac99-8829-4720-a388-da88d015d596">RpcMgmtEpEltInqDone</a>



<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>
 

 

