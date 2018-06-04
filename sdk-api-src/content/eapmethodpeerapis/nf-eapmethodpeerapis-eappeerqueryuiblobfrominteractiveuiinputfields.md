---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EapPeerQueryUIBlobFromInteractiveUIInputFields function


## -description


The <b>EapPeerQueryUIBlobFromInteractiveUIInputFields</b> function converts user information into a user BLOB that can be consumed by EAPHost run-time functions. 


## -parameters




### -param dwVersion [in]

The version number of the API. Must be set to zero.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwSizeofUIContextData [in]

The size of the context data in the <i>pUIContextData</i> parameter, in bytes.


### -param pUIContextData [in]

A pointer to a BLOB that contains UI context data, represented as inner pointers to field data. The supplicant obtained these inner pointers from EAPHost run-time functions.


### -param pEapInteractiveUIData [in]

Pointer that receives an <a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive user interface components raised on an EAP supplicant.


### -param pdwSizeOfDataFromInteractiveUI [out]

A pointer to a DWORD that specifies the size of the buffer pointed to by the <i>ppDataFromInteractiveUI</i> parameter, in bytes. If this value is not set to 0, then a pointer to a buffer of the size specified in this parameter must be supplied in the  <i>ppDataFromInteractiveUI</i> parameter. 


### -param ppDataFromInteractiveUI [out]

  A pointer that receives a credentials BLOB that can be used in authentication.
                The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/544d999c-d857-4ca5-b5f8-b15780fc7019">EapPeerFreeMemory</a>, starting at the innermost pointer. If a non-NULL value is supplied for this parameter, meaning that an existing data BLOB is passed to it, the supplied data BLOB will be updated and returned in this parameter.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.


## -remarks



<b>EapPeerQueryUIBlobFromInteractiveUIInputFields</b> can be employed to support Single-Sign-On (SSO). In an SSO scenario, <b>EapPeerQueryUIBlobFromInteractiveUIInputFields</b> is the last API to be called before resuming a regular call sequence. For more information, see <a href="https://msdn.microsoft.com/aac69e89-249d-4bc8-baef-1f0681f9f7ae">Peer Method API Call Sequence</a>.  




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

