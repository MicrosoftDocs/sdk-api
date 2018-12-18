---
UID: NF:tokenbinding.TokenBindingGenerateBinding
title: TokenBindingGenerateBinding function
author: windows-sdk-content
description: Constructs one token binding that contains the exported public key and signature by using the specified key type for the token binding, a target identifier string for creating and retrieving the token binding key, and the unique data.
old-location: security\tokenbindinggeneratebinding.htm
tech.root: seccng
ms.assetid: 4289E3F0-17AC-485B-A326-2C8BECD5CABB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TokenBindingGenerateBinding, TokenBindingGenerateBinding function [Security], security.tokenbindinggeneratebinding, tokenbinding/TokenBindingGenerateBinding
ms.topic: function
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
 - TokenBindingGenerateBinding
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TokenBindingGenerateBinding function


## -description


Constructs one token binding that contains the exported public key and signature by using the specified key type for the token binding, a target identifier string for creating and retrieving the token binding key, and the unique data. This function also returns the token binding identifier, if needed.


## -parameters




### -param keyType [in]

The negotiated key type to use. Use a value from the list of key types that you retrieved by calling the <a href="https://msdn.microsoft.com/583687B6-5A87-4616-A5EE-4FECFF06749E">TokenBindingGetKeyTypesClient</a> function.


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

A pointer that receives the address of the token binding buffer. Use the <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> function to free that memory.


### -param tokenBindingSize [out]

Pointer to a variable that receives the size of the buffer allocated for the <i>tokenBinding</i> parameter, in bytes.


### -param resultData [out, optional]

A pointer that receives the address of the buffer that contains result data that includes the token binding identifier of the token binding that  <b>TokenBindingGenerateBinding</b> generates. Use the <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> function to allocate the memory for this buffer, and the <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> function to free that memory. Specify NULL is you do not need this information.


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingGenerateBinding</b> from user mode.




## -see-also




<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>



<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a>



<a href="https://msdn.microsoft.com/EBF14890-3F7D-4814-93E1-570E81E05DF2">TOKENBINDING_EXTENSION_FORMAT</a>



<a href="https://msdn.microsoft.com/6C34E174-CCC4-451D-82C3-C410C8C92C8C">TOKENBINDING_RESULT_DATA</a>



<a href="https://msdn.microsoft.com/7F126B3E-1033-4C0A-AD5F-0FAD951C85C6">TOKENBINDING_TYPE</a>



<a href="https://msdn.microsoft.com/4258CC92-580E-403C-9AE4-4BB726255464">TokenBindingDeleteBinding</a>



<a href="https://msdn.microsoft.com/583687B6-5A87-4616-A5EE-4FECFF06749E">TokenBindingGetKeyTypesClient</a>
 

 

