---
UID: NF:tokenbinding.TokenBindingGenerateID
title: TokenBindingGenerateID function (tokenbinding.h)
author: windows-sdk-content
description: Constructs the token binding identifier by extracting the signature algorithm from the key type and copying the exported public key.
old-location: security\tokenbindinggenerateid.htm
tech.root: SecCNG
ms.assetid: F3E30DF8-2A1D-445E-914B-62999428BB6F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TokenBindingGenerateID, TokenBindingGenerateID function [Security], security.tokenbindinggenerateid, tokenbinding/TokenBindingGenerateID
ms.topic: function
f1_keywords: 
 - "tokenbinding/TokenBindingGenerateID"
dev_langs:
 - c++
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
 - TokenBindingGenerateID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TokenBindingGenerateID function


## -description


Constructs the token binding identifier by extracting the
signature algorithm from the key type and copying the exported public key.



## -parameters




### -param keyType [in]

The negotiated key type to use. Use a value from the list of key types that you retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesclient">TokenBindingGetKeyTypesClient</a> function.


### -param publicKey [in]

An exported public key blob.


### -param publicKeySize [in]

The size of the exported public key blob.


### -param resultData [out]

A pointer that receives the address of the buffer that is allocated for the token binding result data.  The token binding result data contains the token binding identifier. 

Use the <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> method to free that memory.


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingGenerateID</b> from user mode.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingverifymessage">TokenBindingVerifyMessage</a>
 

 

