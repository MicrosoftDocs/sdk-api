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

# EapPeerGetConfigBlobAndUserBlob function


## -description


The <b>EapPeerGetConfigBlobAndUserBlob</b> method allows EAP method developers to provide the various connection properties and user properties supported by the method. EAPHost invokes this function to create the connection property and user property of the EAP method.


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the EAP authentication session behavior.


### -param eapMethodType [in]

The <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param eapCredential [in]

An <a href="https://msdn.microsoft.com/DC1B9524-2853-404D-A77A-61CB012FCF11">EapCredential</a> structure that contains the credential type and the appropriate credentials.


### -param pdwConfigBlobSize [out]

Receives a pointer to the size, in bytes, of the <i>ppConfigBlob</i> parameter.


### -param ppConfigBlob [out]

Receives a pointer to a pointer that contains a byte buffer with configured connection data.


### -param pdwUserBlobSize [out]

Receives a pointer to the size, in bytes, of the <i>ppUserBlob</i> parameter.


### -param ppUserBlob [out]

Receives a pointer to a pointer that contains a byte buffer with the methods' user data.


### -param ppEapError [out]

 A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -returns



This function should return <b>ERROR_SUCCESS</b> when it is able to generate the correct connection and user blob. In all other cases, it returns the appropriate windows error.




## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a>



<a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a>



<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a>



<a href="https://msdn.microsoft.com/DC1B9524-2853-404D-A77A-61CB012FCF11">EapCredential</a>



<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>
 

 

