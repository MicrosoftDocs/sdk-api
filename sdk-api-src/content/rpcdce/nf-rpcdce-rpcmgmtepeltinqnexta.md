---
UID: NF:rpcdce.RpcMgmtEpEltInqNextA
title: RpcMgmtEpEltInqNextA function (rpcdce.h)
description: The RpcMgmtEpEltInqNext function returns one element from an endpoint map. (RpcMgmtEpEltInqNextA)
helpviewer_keywords: ["RpcMgmtEpEltInqNextA", "rpcdce/RpcMgmtEpEltInqNextA"]
old-location: rpc\rpcmgmtepeltinqnext.htm
tech.root: Rpc
ms.assetid: e1f79435-6868-453b-8237-da52e57ec96f
ms.date: 12/05/2018
ms.keywords: RpcMgmtEpEltInqNext, RpcMgmtEpEltInqNext function [RPC], RpcMgmtEpEltInqNextA, RpcMgmtEpEltInqNextW, _rpc_rpcmgmtepeltinqnext, rpc.rpcmgmtepeltinqnext, rpcdce/RpcMgmtEpEltInqNext, rpcdce/RpcMgmtEpEltInqNextA, rpcdce/RpcMgmtEpEltInqNextW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcMgmtEpEltInqNextW (Unicode) and RpcMgmtEpEltInqNextA (ANSI)
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
 - RpcMgmtEpEltInqNextA
 - rpcdce/RpcMgmtEpEltInqNextA
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
 - RpcMgmtEpEltInqNext
 - RpcMgmtEpEltInqNextA
 - RpcMgmtEpEltInqNextW
---

# RpcMgmtEpEltInqNextA function


## -description

The 
<b>RpcMgmtEpEltInqNext</b> function returns one element from an endpoint map.

## -parameters

### -param InquiryContext

Specifies an inquiry context. The inquiry context is returned from 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin">RpcMgmtEpEltInqBegin</a>.

### -param IfId

Returns the interface identifier of the endpoint-map element.

### -param Binding

Optional. Returns the binding handle from the endpoint-map element.

### -param ObjectUuid

Optional. Returns the object UUID from the endpoint-map element.

### -param Annotation

Optional. Returns the annotation string for the endpoint-map element. When there is no annotation string in the endpoint-map element, the empty string ("") is returned.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcMgmtEpEltInqNext</b> function returns one element from the endpoint map. Elements selected depend on the inquiry context. The selection criteria are determined by <i>InquiryType</i> of the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin">RpcMgmtEpEltInqBegin</a> function that returned <i>InquiryContext</i>.

An application can view all the selected endpoint-map elements by repeatedly calling 
<b>RpcMgmtEpEltInqNext</b>. When all the elements have been viewed, this function returns an RPC_X_NO_MORE_ENTRIES status. The returned elements are unordered.

When the respective arguments are non-NULL, the RPC run-time function library allocates memory for <i>Binding</i> and <i>Annotation</i> on each call to this function. The application is responsible for calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> for each returned <i>Binding</i> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> for each returned <i>Annotation</i>.

After viewing the endpoint-map elements, the application must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqdone">RpcMgmtEpEltInqDone</a> to delete the inquiry context.





> [!NOTE]
> The rpcdce.h header defines RpcMgmtEpEltInqNext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin">RpcMgmtEpEltInqBegin</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcmgmtepeltinqdone">RpcMgmtEpEltInqDone</a>
