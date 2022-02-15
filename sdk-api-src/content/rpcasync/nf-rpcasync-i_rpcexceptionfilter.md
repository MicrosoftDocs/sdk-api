---
UID: NF:rpcasync.I_RpcExceptionFilter
title: I_RpcExceptionFilter
description: Determines whether an exception is fatal or non-fatal
tech.root: rpc
helpviewer_keywords: ["I_RpcExceptionFilter"]
ms.date: 4/26/2019
ms.keywords: I_RpcExceptionFilter
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: rpcasync.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - I_RpcExceptionFilter
 - rpcasync/I_RpcExceptionFilter
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - rpcrt4.dll
api_name:
 - I_RpcExceptionFilter
---

## -description

Determines whether an exception is fatal or non-fatal

## -parameters

### -param ExceptionCode

Value of an exception. Any of the following exception values will return EXCEPTION_CONTINUE_SEARCH:

- STATUS_ACCESS_VIOLATION
- STATUS_POSSIBLE_DEADLOCK
- STATUS_INSTRUCTION_MISALIGNMENT
- STATUS_DATATYPE_MISALIGNMENT
- STATUS_PRIVILEGED_INSTRUCTION
- STATUS_ILLEGAL_INSTRUCTION
- STATUS_BREAKPOINT
- STATUS_STACK_OVERFLOW
- STATUS_HANDLE_NOT_CLOSABLE
- STATUS_IN_PAGE_ERROR
- STATUS_ASSERTION_FAILURE
- STATUS_STACK_BUFFER_OVERRUN
- STATUS_GUARD_PAGE_VIOLATION
- STATUS_REG_NAT_CONSUMPTION

## -returns

A value that specifies whether the exception was fatal or non-fatal.

| Return code | Description
|-------------|------------|
| EXCEPTION_CONTINUE_SEARCH | The exception is fatal and must be handled. |
| EXCEPTION_EXECUTE_HANDLER | The exception is not fatal. |

## -remarks

## -see-also

