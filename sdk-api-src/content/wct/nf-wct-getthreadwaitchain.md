---
UID: NF:wct.GetThreadWaitChain
title: GetThreadWaitChain function (wct.h)
description: Retrieves the wait chain for the specified thread.
helpviewer_keywords: ["GetThreadWaitChain","GetThreadWaitChain function","WCT_OUT_OF_PROC_COM_FLAG","WCT_OUT_OF_PROC_CS_FLAG","WCT_OUT_OF_PROC_FLAG","base.getthreadwaitchain","wct/GetThreadWaitChain"]
old-location: base\getthreadwaitchain.htm
tech.root: Debug
ms.assetid: 5b418fa6-1d07-465e-85ea-b7127264eebf
ms.date: 12/05/2018
ms.keywords: GetThreadWaitChain, GetThreadWaitChain function, WCT_OUT_OF_PROC_COM_FLAG, WCT_OUT_OF_PROC_CS_FLAG, WCT_OUT_OF_PROC_FLAG, base.getthreadwaitchain, wct/GetThreadWaitChain
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadWaitChain
 - wct/GetThreadWaitChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-wer-wct-l1-1-0.dll
 - wer.dll
api_name:
 - GetThreadWaitChain
---

# GetThreadWaitChain function


## -description

Retrieves the wait chain for the specified thread.

## -parameters

### -param WctHandle [in]

A handle to the WCT session created by the <a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a> function.

### -param Context [in, optional]

A pointer to an application-defined context structure to be passed to the callback function for an asynchronous session.

### -param Flags [in]

The wait chain retrieval options. This parameter can be one of more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCT_OUT_OF_PROC_COM_FLAG"></a><a id="wct_out_of_proc_com_flag"></a><dl>
<dt><b>WCT_OUT_OF_PROC_COM_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Enumerates all threads of an out-of-proc MTA COM server to find the correct thread identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="WCT_OUT_OF_PROC_CS_FLAG"></a><a id="wct_out_of_proc_cs_flag"></a><dl>
<dt><b>WCT_OUT_OF_PROC_CS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Retrieves critical-section information from other processes.

</td>
</tr>
<tr>
<td width="40%"><a id="WCT_OUT_OF_PROC_FLAG"></a><a id="wct_out_of_proc_flag"></a><dl>
<dt><b>WCT_OUT_OF_PROC_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Follows the wait chain into other processes. Otherwise, the function reports the first thread in a different process but does not retrieve additional information.

</td>
</tr>
</table>

### -param ThreadId [in]

The identifier of the thread.

### -param NodeCount [in, out]

On input, a number from 1 to WCT_MAX_NODE_COUNT that specifies the number of nodes in the wait chain. On return, the number of nodes retrieved. If the array cannot contain all the nodes of the wait chain, the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_MORE_DATA, and this parameter receives the number of array elements required to contain all the nodes.

For asynchronous sessions, check the value that is passed to the callback function. Do not free the variable until the callback function has returned.

### -param NodeInfoArray [out]

An array of <a href="/windows/desktop/api/wct/ns-wct-waitchain_node_info">WAITCHAIN_NODE_INFO</a> structures that receives the wait chain.

For asynchronous sessions, check the value that is passed to the callback function. Do not free the array until the callback function has returned.

### -param IsCycle [out]

If the function detects a deadlock, this variable is set to <b>TRUE</b>; otherwise, it is set to <b>FALSE</b>.

For asynchronous sessions, check the value that is passed to the callback function. Do not free the variable until the callback function has returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller did not have sufficient privilege to open a target thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the input parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The WCT session was opened in asynchronous mode. The results will be returned through the <a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a> callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>NodeInfoArray</i> buffer is not large enough to contain all the nodes in the wait chain. The <i>NodeCount</i> parameter contains the number of nodes in the chain. The wait chain returned is still valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The operating system is not providing this service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified thread could not be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TOO_MANY_THREADS</b></dt>
</dl>
</td>
<td width="60%">
The number of nodes exceeds WCT_MAX_NODE_COUNT. The wait chain returned is still valid.

</td>
</tr>
</table>

## -remarks

If the session is asynchronous, the function returns <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_IO_PENDING. To obtain the results, see the <a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a> callback function.

If the specified thread is not blocked or is blocked on an unsupported synchronization element, the function returns a single item in <i>NodeInfoArray</i>.

The caller must have the SE_DEBUG_NAME privilege. If the caller has insufficient privileges, the function fails if the first thread cannot be accessed. Otherwise, the last node in the array will have its <b>ObjectStatus</b> member set to WctStatusNoAcces.

If any subset of nodes in the array forms a cycle, the function sets the <i>IsCycle</i> parameter to <b>TRUE</b>.

Wait chain information is dynamic; it was correct when the function was called but may be out-of-date by the time it is reviewed by the caller.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/using-wct">Using WCT</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a>



<a href="/windows/desktop/api/wct/ns-wct-waitchain_node_info">WAITCHAIN_NODE_INFO</a>



<a href="/windows/desktop/Debug/wait-chain-traversal">Wait Chain Traversal</a>



<a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a>