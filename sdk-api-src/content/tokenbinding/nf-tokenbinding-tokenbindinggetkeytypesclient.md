---
UID: NF:tokenbinding.TokenBindingGetKeyTypesClient
title: TokenBindingGetKeyTypesClient function (tokenbinding.h)
author: windows-sdk-content
description: Retrieves a list of the key types that the client device supports.
old-location: security\tokenbindinggetkeytypesclient.htm
tech.root: SecCNG
ms.assetid: 583687B6-5A87-4616-A5EE-4FECFF06749E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TokenBindingGetKeyTypesClient, TokenBindingGetKeyTypesClient function [Security], security.tokenbindinggetkeytypesclient, tokenbinding/TokenBindingGetKeyTypesClient
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
 - TokenBindingGetKeyTypesClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TokenBindingGetKeyTypesClient function


## -description


Retrieves a list of the key types that the client device supports.


## -parameters




### -param keyTypes [out]

A pointer to a buffer that contains the list of key types that the client device supports. <b>TokenBindingGetKeyTypesClient</b> returns the string identifiers for well-known algorithms that correspond to the keys that the client device supports. Use <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> to allocate the memory for the buffer, and <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> to free that memory. 


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingGetKeyTypesClient</b> from user mode.




## -see-also




<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>



<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a>



<a href="https://msdn.microsoft.com/E5029CE3-CD23-4566-A951-35374DC7BC57">TOKENBINDING_KEY_TYPES</a>



<a href="https://msdn.microsoft.com/8ABAC0AF-AF68-4742-9C36-3FB17D303409">TokenBindingGetKeyTypesServer</a>
 

 

