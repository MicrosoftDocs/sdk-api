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

# RpcExceptionFilter function


## -description


The <b>RpcExceptionFilter</b> function is a default exception filter that determines whether an exception is fatal or non-fatal.<b>RpcExceptionFilter</b> is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with <a href="https://msdn.microsoft.com/5bd57250-1fd7-4aeb-aa53-4fd2c8d84836">RpcExcept</a>.


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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
RpcTry
{
    … RPC calls here …
RpcExcept(RpcExceptionFilter(RpcExceptionCode()))
{
    … error handling here …
}
RpcEndExcept</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7133d3f4-ed84-4cde-bc77-88e73ced9073">Exception Handling</a>



<a href="https://msdn.microsoft.com/5bd57250-1fd7-4aeb-aa53-4fd2c8d84836">RpcExcept</a>



<a href="https://msdn.microsoft.com/9a61f6aa-b1da-48e2-bf4c-251f729ab766">RpcExceptionCode</a>



<a href="https://msdn.microsoft.com/3addb367-4bdc-4c11-bf4d-b5b94da45b26">RpcTryExcept</a>
 

 

