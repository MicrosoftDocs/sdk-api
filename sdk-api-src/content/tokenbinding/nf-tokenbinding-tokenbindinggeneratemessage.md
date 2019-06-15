---
UID: NF:tokenbinding.TokenBindingGenerateMessage
title: TokenBindingGenerateMessage function (tokenbinding.h)
author: windows-sdk-content
description: Assembles the list of token bindings and generates the final message for the client device to the server.
old-location: security\tokenbindinggeneratemessage.htm
tech.root: SecCNG
ms.assetid: 7A268C6D-952B-482A-835D-89D6452D986D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TokenBindingGenerateMessage, TokenBindingGenerateMessage function [Security], security.tokenbindinggeneratemessage, tokenbinding/TokenBindingGenerateMessage
ms.topic: function
f1_keywords: ["tokenbinding/TokenBindingGenerateMessage"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
api_name:
 - TokenBindingGenerateMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TokenBindingGenerateMessage function


## -description


Assembles the list of token bindings and generates the final message for the client device to the server.


## -parameters




### -param tokenBindings [in]

Pointer to an array of token binding structures.


### -param tokenBindingsSize [in]

An array that contains the sizes of the corresponding token binding structures that the array in the <i>tokenBindings</i> parameter contains, in bytes. 


### -param tokenBindingsCount [in]

The number of elements that the array in the <i>tokenBindings</i> parameter contains. This value cannot be 0.


### -param tokenBindingMessage [out]

A pointer that receives the address of the buffer that is allocated for the token binding message.  Use the <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> method to free that memory.


### -param tokenBindingMessageSize [out]

A pointer to a variable that contains the size of the buffer allocated for the <i>tokenBindingMessage</i> parameter.


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingGenerateMessage</b> from user mode.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingverifymessage">TokenBindingVerifyMessage</a>
 

 

