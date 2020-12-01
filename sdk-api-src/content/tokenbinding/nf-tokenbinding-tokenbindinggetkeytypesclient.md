---
UID: NF:tokenbinding.TokenBindingGetKeyTypesClient
title: TokenBindingGetKeyTypesClient function (tokenbinding.h)
description: Retrieves a list of the key types that the client device supports.
helpviewer_keywords: ["TokenBindingGetKeyTypesClient","TokenBindingGetKeyTypesClient function [Security]","security.tokenbindinggetkeytypesclient","tokenbinding/TokenBindingGetKeyTypesClient"]
old-location: security\tokenbindinggetkeytypesclient.htm
tech.root: security
ms.assetid: 583687B6-5A87-4616-A5EE-4FECFF06749E
ms.date: 12/05/2018
ms.keywords: TokenBindingGetKeyTypesClient, TokenBindingGetKeyTypesClient function [Security], security.tokenbindinggetkeytypesclient, tokenbinding/TokenBindingGetKeyTypesClient
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
req.dll: Tokenbinding.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TokenBindingGetKeyTypesClient
 - tokenbinding/TokenBindingGetKeyTypesClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
api_name:
 - TokenBindingGetKeyTypesClient
---

# TokenBindingGetKeyTypesClient function


## -description

Retrieves a list of the key types that the client device supports.

## -parameters

### -param keyTypes [out]

A pointer to a buffer that contains the list of key types that the client device supports. <b>TokenBindingGetKeyTypesClient</b> returns the string identifiers for well-known algorithms that correspond to the keys that the client device supports. Use <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> to allocate the memory for the buffer, and <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> to free that memory.

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can call <b>TokenBindingGetKeyTypesClient</b> from user mode.

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_key_types">TOKENBINDING_KEY_TYPES</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesserver">TokenBindingGetKeyTypesServer</a>