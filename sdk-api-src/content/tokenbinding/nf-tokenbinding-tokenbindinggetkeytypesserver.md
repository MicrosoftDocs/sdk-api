---
UID: NF:tokenbinding.TokenBindingGetKeyTypesServer
title: TokenBindingGetKeyTypesServer function (tokenbinding.h)
description: Retrieves a list of the key types that the server supports.
helpviewer_keywords: ["TokenBindingGetKeyTypesServer","TokenBindingGetKeyTypesServer function [Security]","security.tokenbindinggetkeytypesserver","tokenbinding/TokenBindingGetKeyTypesServer"]
old-location: security\tokenbindinggetkeytypesserver.htm
tech.root: security
ms.assetid: 8ABAC0AF-AF68-4742-9C36-3FB17D303409
ms.date: 12/05/2018
ms.keywords: TokenBindingGetKeyTypesServer, TokenBindingGetKeyTypesServer function [Security], security.tokenbindinggetkeytypesserver, tokenbinding/TokenBindingGetKeyTypesServer
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tokenbinding.lib
req.dll: Tokenbinding.dll (user mode); Ksecdd.sys (kernel mode)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TokenBindingGetKeyTypesServer
 - tokenbinding/TokenBindingGetKeyTypesServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
 - Ksecdd.sys
api_name:
 - TokenBindingGetKeyTypesServer
---

# TokenBindingGetKeyTypesServer function


## -description

Retrieves a list of the key types that the server supports.

## -parameters

### -param keyTypes [out]

A pointer to a buffer that contains the list of key types that the server supports. <b>TokenBindingGetKeyTypesServer</b> returns the string identifiers for well-known algorithms that correspond to the keys that the server supports.

In user mode, use <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> to allocate the memory for the buffer, and <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> to free that memory. In kernel mode, use <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>  to allocate the memory for the buffer, and <a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-exfreepool">ExFreePool</a> to free that memory.

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can call <b>TokenBindingGetKeyTypesServer</b> from both user mode and kernel mode. To call this function in kernel mode,  link to Ksecdd.sys, and use the functions mentioned in the description for the <i>keyTypes</i> parameter for allocating and freeing memory.

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_key_types">TOKENBINDING_KEY_TYPES</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesclient">TokenBindingGetKeyTypesClient</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingverifymessage">TokenBindingVerifyMessage</a>