---
UID: NF:tokenbinding.TokenBindingGenerateBinding
title: TokenBindingGenerateBinding function (tokenbinding.h)
description: Constructs one token binding that contains the exported public key and signature by using the specified key type for the token binding, a target identifier string for creating and retrieving the token binding key, and the unique data.
helpviewer_keywords: ["TokenBindingGenerateBinding","TokenBindingGenerateBinding function [Security]","security.tokenbindinggeneratebinding","tokenbinding/TokenBindingGenerateBinding"]
old-location: security\tokenbindinggeneratebinding.htm
tech.root: security
ms.assetid: 4289E3F0-17AC-485B-A326-2C8BECD5CABB
ms.date: 12/05/2018
ms.keywords: TokenBindingGenerateBinding, TokenBindingGenerateBinding function [Security], security.tokenbindinggeneratebinding, tokenbinding/TokenBindingGenerateBinding
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
 - TokenBindingGenerateBinding
 - tokenbinding/TokenBindingGenerateBinding
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
 - TokenBindingGenerateBinding
---

# TokenBindingGenerateBinding function


## -description

Constructs one token binding that contains the exported public key and signature by using the specified key type for the token binding, a target identifier string for creating and retrieving the token binding key, and the unique data. This function also returns the token binding identifier, if needed.

## -parameters

### -param keyType [in]

The negotiated key type to use. Use a value from the list of key types that you retrieved by calling the <a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesclient">TokenBindingGetKeyTypesClient</a> function.

### -param targetURL [in]

The target string to use in conjunction with the key type  to generate or retrieve a token binding key for the NCrypt operations that build the buffer for the <i>tokenBinding</i> parameter.

### -param bindingType [in]

The type of token binding that <b>TokenBindingGenerateBinding</b> should generate.

### -param tlsEKM [in]

A pointer to the buffer that contains unique data.

### -param tlsEKMSize [in]

The size of the buffer that the <i>tlsUnique</i> parameter points to, in bytes.

### -param extensionFormat [in]

The format to use to interpret the data in the <i>extensionData</i> parameter. This value must be <b>TOKENBINDING_EXTENSION_FORMAT_UNDEFINED</b>.

### -param extensionData [in]

A pointer to a buffer that contains extension data. The value of the <i>extensionFormat</i> parameter determines how to interpret this data.

### -param tokenBinding [out]

A pointer that receives the address of the token binding buffer. Use the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> function to free that memory.

### -param tokenBindingSize [out]

Pointer to a variable that receives the size of the buffer allocated for the <i>tokenBinding</i> parameter, in bytes.

### -param resultData [out, optional]

A pointer that receives the address of the buffer that contains result data that includes the token binding identifier of the token binding that  <b>TokenBindingGenerateBinding</b> generates. Use the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> function to free that memory. Specify NULL is you do not need this information.

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can call <b>TokenBindingGenerateBinding</b> from user mode.

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="/windows/desktop/api/tokenbinding/ne-tokenbinding-tokenbinding_extension_format">TOKENBINDING_EXTENSION_FORMAT</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_result_data">TOKENBINDING_RESULT_DATA</a>



<a href="/windows/desktop/api/tokenbinding/ne-tokenbinding-tokenbinding_type">TOKENBINDING_TYPE</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingdeletebinding">TokenBindingDeleteBinding</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesclient">TokenBindingGetKeyTypesClient</a>