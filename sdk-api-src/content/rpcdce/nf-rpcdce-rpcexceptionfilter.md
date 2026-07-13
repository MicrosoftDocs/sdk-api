---
UID: NF:rpcdce.RpcExceptionFilter
title: RpcExceptionFilter function (rpcdce.h)
description: A default exception filter that determines whether an exception is fatal or non-fatal.
helpviewer_keywords: ["RpcExceptionFilter","RpcExceptionFilter function [RPC]","STATUS_ACCESS_VIOLATION","STATUS_ASSERTION_FAILURE","STATUS_BREAKPOINT","STATUS_DATATYPE_MISALIGNMENT","STATUS_GUARD_PAGE_VIOLATION","STATUS_HANDLE_NOT_CLOSABLE","STATUS_ILLEGAL_INSTRUCTION","STATUS_INSTRUCTION_MISALIGNMENT","STATUS_IN_PAGE_ERROR","STATUS_POSSIBLE_DEADLOCK","STATUS_PRIVILEGED_INSTRUCTION","STATUS_REG_NAT_CONSUMPTION","STATUS_STACK_BUFFER_OVERRUN","STATUS_STACK_OVERFLOW","rpc.rpcexceptionfilter","rpcdce/RpcExceptionFilter"]
old-location: rpc\rpcexceptionfilter.htm
tech.root: Rpc
ms.assetid: AB1AE035-5874-4415-8B85-BDC0E2139416
ms.date: 12/05/2018
ms.keywords: RpcExceptionFilter, RpcExceptionFilter function [RPC], STATUS_ACCESS_VIOLATION, STATUS_ASSERTION_FAILURE, STATUS_BREAKPOINT, STATUS_DATATYPE_MISALIGNMENT, STATUS_GUARD_PAGE_VIOLATION, STATUS_HANDLE_NOT_CLOSABLE, STATUS_ILLEGAL_INSTRUCTION, STATUS_INSTRUCTION_MISALIGNMENT, STATUS_IN_PAGE_ERROR, STATUS_POSSIBLE_DEADLOCK, STATUS_PRIVILEGED_INSTRUCTION, STATUS_REG_NAT_CONSUMPTION, STATUS_STACK_BUFFER_OVERRUN, STATUS_STACK_OVERFLOW, rpc.rpcexceptionfilter, rpcdce/RpcExceptionFilter
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - RpcExceptionFilter
 - rpcdce/RpcExceptionFilter
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
 - RpcExceptionFilter
---

# RpcExceptionFilter function


## -description

The <b>RpcExceptionFilter</b> function is a default exception filter that determines whether an exception is fatal or non-fatal. <b>RpcExceptionFilter</b> is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with <a href="/windows/desktop/api/rpc/nf-rpc-rpcexcept">RpcExcept</a>.

## -parameters

### -param ExceptionCode [in]

Value of an exception. Any of the following exception values will return <b>EXCEPTION_CONTINUE_SEARCH</b>:

<a id="STATUS_ACCESS_VIOLATION"></a>
<a id="status_access_violation"></a>


#### STATUS_ACCESS_VIOLATION

<a id="STATUS_POSSIBLE_DEADLOCK"></a>
<a id="status_possible_deadlock"></a>


#### STATUS_POSSIBLE_DEADLOCK

<a id="STATUS_INSTRUCTION_MISALIGNMENT_"></a>
<a id="status_instruction_misalignment_"></a>


#### STATUS_INSTRUCTION_MISALIGNMENT

<a id="STATUS_DATATYPE_MISALIGNMENT"></a>
<a id="status_datatype_misalignment"></a>


#### STATUS_DATATYPE_MISALIGNMENT

<a id="STATUS_PRIVILEGED_INSTRUCTION"></a>
<a id="status_privileged_instruction"></a>


#### STATUS_PRIVILEGED_INSTRUCTION

<a id="STATUS_ILLEGAL_INSTRUCTION"></a>
<a id="status_illegal_instruction"></a>


#### STATUS_ILLEGAL_INSTRUCTION

<a id="STATUS_BREAKPOINT"></a>
<a id="status_breakpoint"></a>


#### STATUS_BREAKPOINT

<a id="STATUS_STACK_OVERFLOW"></a>
<a id="status_stack_overflow"></a>


#### STATUS_STACK_OVERFLOW

<a id="STATUS_HANDLE_NOT_CLOSABLE"></a>
<a id="status_handle_not_closable"></a>


#### STATUS_HANDLE_NOT_CLOSABLE

<a id="STATUS_IN_PAGE_ERROR"></a>
<a id="status_in_page_error"></a>


#### STATUS_IN_PAGE_ERROR

<a id="STATUS_ASSERTION_FAILURE"></a>
<a id="status_assertion_failure"></a>


#### STATUS_ASSERTION_FAILURE

<a id="STATUS_STACK_BUFFER_OVERRUN"></a>
<a id="status_stack_buffer_overrun"></a>


#### STATUS_STACK_BUFFER_OVERRUN

<a id="STATUS_GUARD_PAGE_VIOLATION"></a>
<a id="status_guard_page_violation"></a>


#### STATUS_GUARD_PAGE_VIOLATION

<a id="STATUS_REG_NAT_CONSUMPTION"></a>
<a id="status_reg_nat_consumption"></a>


#### STATUS_REG_NAT_CONSUMPTION

## -returns

A value that specifies whether the exception was fatal or non-fatal.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXCEPTION_CONTINUE_SEARCH</b></dt>
</dl>
</td>
<td width="60%">
The exception is fatal and must be handled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXCEPTION_EXECUTE_HANDLER</b></dt>
</dl>
</td>
<td width="60%">
The exception is not fatal.

</td>
</tr>
</table>

## -remarks

The recommended usage of <b>RpcExceptionFilter</b> is:


```cpp

RpcTry
{
    … RPC calls here …
RpcExcept(RpcExceptionFilter(RpcExceptionCode()))
{
    … error handling here …
}
RpcEndExcept
```

## -see-also

<a href="/windows/desktop/Rpc/exception-handling">Exception Handling</a>



<a href="/windows/desktop/api/rpc/nf-rpc-rpcexcept">RpcExcept</a>



<a href="/previous-versions/aa375695(v=vs.80)">RpcExceptionCode</a>



<a href="/windows/desktop/Rpc/rpctryexcept">RpcTryExcept</a>
