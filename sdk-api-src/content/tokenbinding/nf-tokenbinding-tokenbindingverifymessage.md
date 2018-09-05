---
UID: NF:tokenbinding.TokenBindingVerifyMessage
title: TokenBindingVerifyMessage function
author: windows-sdk-content
description: Validates the token binding message and verifies the token bindings that the message contains.
old-location: security\tokenbindingverifymessage.htm
old-project: SecCNG
ms.assetid: D6827DA3-75DC-4F31-B57A-4ED5B5F03112
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: TokenBindingVerifyMessage, TokenBindingVerifyMessage function [Security], security.tokenbindingverifymessage, tokenbinding/TokenBindingVerifyMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tokenbinding.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TOKENBINDING_TYPE
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
product: Windows
targetos: Windows
req.lib: Tokenbinding.lib
req.dll: Tokenbinding.dll (user mode); Ksecdd.sys (kernel mode)
req.irql: 
req.product: Windows XP with SP1 and later
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

The negotiated key algorithm to use. Use a value from the list of key types that you retrieved by calling the <a href="https://msdn.microsoft.com/8ABAC0AF-AF68-4742-9C36-3FB17D303409">TokenBindingGetKeyTypesServer</a> function.


### -param tlsEKM [in]

A pointer to a buffer that contains unique data.


### -param tlsEKMSize [in]

The size of the buffer that the <i>tlsUnique</i> parameter points to, in bytes.


### -param resultList [out]

A pointer that receives the address for the buffer that contains the results for each of the token bindings that <b>TokenBindingVerifyMessage</b>   verifies.

In user mode, use <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> to allocate the memory for the buffer, and <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> to free that memory. In kernel mode, use <a href="https://msdn.microsoft.com/a9951e7b-60a2-4bf2-913c-b7291d7c3173">ExAllocatePoolWithTag</a>  to allocate the memory for the buffer, and <a href="https://msdn.microsoft.com/c26f9b28-396d-40de-bdc3-287fc3ac4113">ExFreePool</a> to free that memory.


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingVerifyMessage</b> from both user mode and kernel mode. o call this function in kernel mode,  link to Ksecdd.sys, and use the functions mentioned in the description for the <i>resultList</i> parameter for allocating and freeing memory.




## -see-also




<a href="https://msdn.microsoft.com/a9951e7b-60a2-4bf2-913c-b7291d7c3173">ExAllocatePoolWithTag</a>



<a href="https://msdn.microsoft.com/c26f9b28-396d-40de-bdc3-287fc3ac4113">ExFreePool</a>



<a href="https://msdn.microsoft.com/D14CBEA3-5F46-4C45-8C11-407D6E70FD56">TOKENBINDING_RESULT_LIST</a>



<a href="https://msdn.microsoft.com/7A268C6D-952B-482A-835D-89D6452D986D">TokenBindingGenerateMessage</a>



<a href="https://msdn.microsoft.com/8ABAC0AF-AF68-4742-9C36-3FB17D303409">TokenBindingGetKeyTypesServer</a>
 

 

