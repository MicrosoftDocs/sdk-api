---
UID: NC:ntsecpkg.SpUnsealMessageFn
title: SpUnsealMessageFn (ntsecpkg.h)
author: windows-sdk-content
description: Decrypts a message that was previously encrypted with the SpSealMessage function.
old-location: security\spunsealmessage.htm
tech.root: SecAuthN
ms.assetid: 3ece6f30-bb8b-4fad-a8c4-9088c134cf25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpUnsealMessage, SpUnsealMessage callback function [Security], SpUnsealMessageFn, SpUnsealMessageFn callback, _ssp_spunsealmessage, ntsecpkg/SpUnsealMessage, security.spunsealmessage
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpUnsealMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpUnsealMessageFn callback function


## -description


Decrypts a message that was previously encrypted with the 
<a href="https://msdn.microsoft.com/400bc3e7-e9a1-4267-b4de-44d79dceb9e5">SpSealMessage</a> function.

The <b>SpUnsealMessage</b> function is the dispatch function for the 
<a href="https://msdn.microsoft.com/ea271d0c-9167-41c5-8919-09611206fc71">DecryptMessage (General)</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param ContextHandle [in]

Handle of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> used to seal the message.


### -param MessageBuffers [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains the message buffers and a signature buffer.


### -param MessageSequenceNumber [in]

Sequence number to assign to the message. Sequence numbers are optional and are used as protection against loss and insertion of messages. A value of zero indicates that sequence numbers are not in use.


### -param QualityOfProtection [out]

Not used.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpUnsealMessage</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpUnsealMessage</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ea271d0c-9167-41c5-8919-09611206fc71">DecryptMessage (General)</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/400bc3e7-e9a1-4267-b4de-44d79dceb9e5">SpSealMessage</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

