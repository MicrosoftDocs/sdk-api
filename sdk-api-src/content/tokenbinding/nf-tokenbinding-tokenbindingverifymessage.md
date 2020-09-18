---
UID: NF:tokenbinding.TokenBindingVerifyMessage
title: TokenBindingVerifyMessage function (tokenbinding.h)
description: Validates the token binding message and verifies the token bindings that the message contains.
helpviewer_keywords: ["TokenBindingVerifyMessage","TokenBindingVerifyMessage function [Security]","security.tokenbindingverifymessage","tokenbinding/TokenBindingVerifyMessage"]
old-location: security\tokenbindingverifymessage.htm
tech.root: security
ms.assetid: D6827DA3-75DC-4F31-B57A-4ED5B5F03112
ms.date: 12/05/2018
ms.keywords: TokenBindingVerifyMessage, TokenBindingVerifyMessage function [Security], security.tokenbindingverifymessage, tokenbinding/TokenBindingVerifyMessage
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
 - TokenBindingVerifyMessage
 - tokenbinding/TokenBindingVerifyMessage
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
 - TokenBindingVerifyMessage
---

# TokenBindingVerifyMessage function


## -description

Validates the token binding message and verifies the token bindings that the message contains.

## -parameters

### -param tokenBindingMessage [in]

A pointer to the buffer that contains the token binding message.

### -param tokenBindingMessageSize [in]

The size of the buffer that the <i>tokenBindingMessage</i> parameter points to, in bytes.

### -param keyType [in]

The negotiated key algorithm to use. Use a value from the list of key types that you retrieved by calling the <a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesserver">TokenBindingGetKeyTypesServer</a> function.

### -param tlsEKM [in]

A pointer to a buffer that contains unique data.

### -param tlsEKMSize [in]

The size of the buffer that the <i>tlsUnique</i> parameter points to, in bytes.

### -param resultList [out]

A pointer that receives the address for the buffer that contains the results for each of the token bindings that <b>TokenBindingVerifyMessage</b>   verifies.

In user mode, use <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> to allocate the memory for the buffer, and <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> to free that memory. In kernel mode, use <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>  to allocate the memory for the buffer, and <a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-exfreepool">ExFreePool</a> to free that memory.

## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can call <b>TokenBindingVerifyMessage</b> from both user mode and kernel mode. o call this function in kernel mode,  link to Ksecdd.sys, and use the functions mentioned in the description for the <i>resultList</i> parameter for allocating and freeing memory.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-exallocatepoolwithtag">ExAllocatePoolWithTag</a>



<a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-exfreepool">ExFreePool</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_result_list">TOKENBINDING_RESULT_LIST</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggeneratemessage">TokenBindingGenerateMessage</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesserver">TokenBindingGetKeyTypesServer</a>