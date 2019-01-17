---
UID: NF:rpc.RpcExcept
title: RpcExcept macro
author: windows-sdk-content
description: The RpcExcept statement provides structured exception handling for RPC applications.
old-location: rpc\rpcexcept.htm
tech.root: Rpc
ms.assetid: 5bd57250-1fd7-4aeb-aa53-4fd2c8d84836
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcExcept, RpcExcept macro [RPC], _rpc_rpcexcept, rpc.rpcexcept, rpc/RpcExcept
ms.topic: macro
req.header: rpc.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpc.h
api_name:
 - RpcExcept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcExcept macro


## -description


The 
<b>RpcExcept</b> statement provides structured exception handling for RPC applications.

<b>Windows Vista and later versions of Windows:  </b><a href="https://msdn.microsoft.com/AB1AE035-5874-4415-8B85-BDC0E2139416">RpcExceptionFilter</a> is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with <b>RpcExcept</b>. Custom exception filters must still use <b>RpcExcept</b>, however.


## -parameters




### -param expr

Expression that is evaluated when an exception occurs. If <i>expression</i> evaluates to a nonzero value, the exception statements are executed. If <i>expression</i> evaluates to a zero value, unwinding continues to the next 
<a href="https://msdn.microsoft.com/3addb367-4bdc-4c11-bf4d-b5b94da45b26">RpcTryExcept</a> or 
<a href="https://msdn.microsoft.com/e9ed748a-db15-4c91-b8a4-b510f99042d8">RpcTryFinally</a> function.


## -remarks



If an exception does not occur, the <i>expression</i> and <i>exception statements</i> are skipped and execution continues at the statement following the 
<a href="https://msdn.microsoft.com/fcf0270c-6172-465b-87c9-d15693608183">RpcEndExcept</a> statement.

The compound statement after the 
<b>RpcTryExcept</b> clause is the body or guarded section. The compound statement after the 
<b>RpcExcept</b> clause is the exception handler. The handler specifies a set of actions to be taken if an exception is raised during execution of the body of the guarded section. Execution proceeds as follows:

<ol>
<li>The guarded section is executed.</li>
<li>If no exception occurs during execution of the guarded section, execution continues at the statement after 
<b>RpcEndExcept</b> clause.</li>
<li>If an exception occurs during execution of the guarded section or in any routine the guarded section calls, the __except expression is evaluated and the value determines how the exception is handled. There are three values: 


<ul>
<li>EXCEPTION_CONTINUE_EXECUTION (–1) Exception is dismissed. Continue execution at the point where the exception occurred.</li>
<li>EXCEPTION_CONTINUE_SEARCH (0) Exception is not recognized. Continue to search up the stack for a handler, first for containing try-except statements, then for handlers with the next highest precedence.</li>
<li>Exception is recognized. Transfer control to the exception handler by executing the __except compound statement, then continue execution after the __except block.</li>
</ul>
</li>
</ol>
Because the 
<b>RpcExcept</b> expression is evaluated as a C expression, it is limited to a single value, the conditional-expression operator, or the comma operator. If more extensive processing is required, the expression can call a routine that returns one of the three values listed above.


<a href="https://msdn.microsoft.com/9a61f6aa-b1da-48e2-bf4c-251f729ab766">RpcExceptionCode</a> can be used in both <i>expression</i> and <i>exception statements</i> to determine which exception occurred.

The following restrictions apply:

<ul>
<li>Jumping (through a <b>goto</b>) into <i>guarded statements</i> is not allowed.</li>
<li>Jumping (through a <b>goto</b>) into <i>exception statements</i> is not allowed.</li>
<li>Returning or jumping (through a <b>goto</b>) from <i>guarded statements</i> is not allowed.</li>
<li>Returning or jumping (through a <b>goto</b>) from <i>exception statements</i> is not allowed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7133d3f4-ed84-4cde-bc77-88e73ced9073">Exception Handling</a>



<a href="https://msdn.microsoft.com/9a61f6aa-b1da-48e2-bf4c-251f729ab766">RpcExceptionCode</a>



<a href="https://msdn.microsoft.com/AB1AE035-5874-4415-8B85-BDC0E2139416">RpcExceptionFilter</a>



<a href="https://msdn.microsoft.com/332641ea-748f-47e5-bb0e-33d2bf4e04c9">RpcFinally</a>



<a href="https://msdn.microsoft.com/0bffc62e-a80e-4af1-a17a-ef4f00b9c4da">RpcRaiseException</a>
 

 

