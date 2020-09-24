---
UID: NC:wct.PWAITCHAINCALLBACK
title: PWAITCHAINCALLBACK (wct.h)
description: An application-defined callback function that receives a wait chain. Specify this address when calling the OpenThreadWaitChainSession function.
helpviewer_keywords: ["ERROR_ACCESS_DENIED","ERROR_CANCELLED","ERROR_MORE_DATA","ERROR_OBJECT_NOT_FOUND","ERROR_SUCCESS","ERROR_TOO_MANY_THREADS","PWAITCHAINCALLBACK","PWAITCHAINCALLBACK callback","PWAITCHAINCALLBACK callback function","base.waitchaincallback","wct/PWAITCHAINCALLBACK"]
old-location: base\waitchaincallback.htm
tech.root: Debug
ms.assetid: 07d987b4-3ee4-4957-a6e8-542c427b94dd
ms.date: 12/05/2018
ms.keywords: ERROR_ACCESS_DENIED, ERROR_CANCELLED, ERROR_MORE_DATA, ERROR_OBJECT_NOT_FOUND, ERROR_SUCCESS, ERROR_TOO_MANY_THREADS, PWAITCHAINCALLBACK, PWAITCHAINCALLBACK callback, PWAITCHAINCALLBACK callback function, base.waitchaincallback, wct/PWAITCHAINCALLBACK
req.header: wct.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWAITCHAINCALLBACK
 - wct/PWAITCHAINCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wct.h
api_name:
 - PWAITCHAINCALLBACK
---

# PWAITCHAINCALLBACK callback function


## -description

An application-defined callback function that receives a wait chain. Specify this address when calling the 
<a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a> function.

The <b>PWAITCHAINCALLBACK</b> type defines a pointer to this callback function. 
<i>WaitChainCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param WctHandle

A handle to the WCT session created by the <a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a> function.

### -param Context

A optional pointer to an application-defined context structure specified by the <a href="/windows/desktop/api/wct/nf-wct-getthreadwaitchain">GetThreadWaitChain</a> function.

### -param CallbackStatus

The callback status. This parameter can be one of the following values, or one of the other <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ERROR_ACCESS_DENIED"></a><a id="error_access_denied"></a><dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller did not have sufficient privilege to open a target thread.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_CANCELLED"></a><a id="error_cancelled"></a><dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous session was canceled by a call to the <a href="/windows/desktop/api/wct/nf-wct-closethreadwaitchainsession">CloseThreadWaitChainSession</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_MORE_DATA"></a><a id="error_more_data"></a><dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>NodeInfoArray</i> buffer is not large enough to contain all the nodes in the wait chain. The <i>NodeCount</i> parameter contains the number of nodes in the chain. The wait chain returned is still valid.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_OBJECT_NOT_FOUND"></a><a id="error_object_not_found"></a><dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified thread could not be located.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_SUCCESS"></a><a id="error_success"></a><dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="ERROR_TOO_MANY_THREADS"></a><a id="error_too_many_threads"></a><dl>
<dt><b>ERROR_TOO_MANY_THREADS</b></dt>
</dl>
</td>
<td width="60%">
The number of nodes exceeds WCT_MAX_NODE_COUNT. The wait chain returned is still valid.

</td>
</tr>
</table>

### -param NodeCount

The number of nodes retrieved, up to WCT_MAX_NODE_COUNT. If the array cannot contain all the nodes of the wait chain, the function fails, <i>CallbackStatus</i> is ERROR_MORE_DATA, and this parameter receives the number of array elements required to contain all the nodes.

### -param NodeInfoArray

An array of <a href="/windows/desktop/api/wct/ns-wct-waitchain_node_info">WAITCHAIN_NODE_INFO</a> structures that receives the wait chain.

### -param IsCycle

If the function detects a deadlock, this variable is set to <b>TRUE</b>; otherwise, it is set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wct/nf-wct-getthreadwaitchain">GetThreadWaitChain</a>



<a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a>



<a href="/windows/desktop/api/wct/ns-wct-waitchain_node_info">WAITCHAIN_NODE_INFO</a>