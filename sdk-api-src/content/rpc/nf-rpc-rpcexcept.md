---
UID: NF:rpc.RpcExcept
title: RpcExcept macro (rpc.h)
description: The RpcExcept statement provides structured exception handling for RPC applications.
helpviewer_keywords: ["RpcExcept","RpcExcept macro [RPC]","_rpc_rpcexcept","rpc.rpcexcept","rpc/RpcExcept"]
old-location: rpc\rpcexcept.htm
tech.root: Rpc
ms.assetid: 5bd57250-1fd7-4aeb-aa53-4fd2c8d84836
ms.date: 12/05/2018
ms.keywords: RpcExcept, RpcExcept macro [RPC], _rpc_rpcexcept, rpc.rpcexcept, rpc/RpcExcept
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcExcept
 - rpc/RpcExcept
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpc.h
api_name:
 - RpcExcept
---

# RpcExcept macro


## -description

The 
<b>RpcExcept</b> statement provides structured exception handling for RPC applications.

<b>Windows Vista and later versions of Windows:  </b><a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcexceptionfilter">RpcExceptionFilter</a> is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with <b>RpcExcept</b>. Custom exception filters must still use <b>RpcExcept</b>, however.

## -parameters

### -param expr

Expression that is evaluated when an exception occurs. If <i>expression</i> evaluates to a nonzero value, the exception statements are executed. If <i>expression</i> evaluates to a zero value, unwinding continues to the next 
<a href="/windows/desktop/Rpc/rpctryexcept">RpcTryExcept</a> or 
<a href="/windows/desktop/Rpc/rpctryfinally">RpcTryFinally</a> function.

## -remarks

If an exception does not occur, the <i>expression</i> and <i>exception statements</i> are skipped and execution continues at the statement following the 
<a href="/previous-versions/aa375629(v=vs.80)">RpcEndExcept</a> statement.

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


<a href="/previous-versions/aa375695(v=vs.80)">RpcExceptionCode</a> can be used in both <i>expression</i> and <i>exception statements</i> to determine which exception occurred.

The following restrictions apply:

<ul>
<li>Jumping (through a <b>goto</b>) into <i>guarded statements</i> is not allowed.</li>
<li>Jumping (through a <b>goto</b>) into <i>exception statements</i> is not allowed.</li>
<li>Returning or jumping (through a <b>goto</b>) from <i>guarded statements</i> is not allowed.</li>
<li>Returning or jumping (through a <b>goto</b>) from <i>exception statements</i> is not allowed.</li>
</ul>

## -see-also

<a href="/windows/desktop/Rpc/exception-handling">Exception Handling</a>



<a href="/previous-versions/aa375695(v=vs.80)">RpcExceptionCode</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcexceptionfilter">RpcExceptionFilter</a>



<a href="/previous-versions/aa375699(v=vs.80)">RpcFinally</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcraiseexception">RpcRaiseException</a>