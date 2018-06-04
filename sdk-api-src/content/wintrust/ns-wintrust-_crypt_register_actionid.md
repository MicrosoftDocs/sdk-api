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

# _CRYPT_REGISTER_ACTIONID structure


## -description


<p class="CCE_Message">[The  <b>CRYPT_REGISTER_ACTIONID</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_REGISTER_ACTIONID</b> structure provides information about the functions of a provider. This structure is used by the  <a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a> function.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field sInitProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the function that initializes the provider.


### -field sObjectProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the object provider function.


### -field sSignatureProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the signature provider function.


### -field sCertificateProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the certificate provider function.


### -field sCertificatePolicyProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the certificate policy provider function.


### -field sFinalPolicyProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the final policy provider function.


### -field sTestPolicyProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the test policy provider function.


### -field sCleanupProvider


<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a> structure that identifies the cleanup provider function.


## -see-also




<a href="https://msdn.microsoft.com/1a531219-f254-4057-934b-af95bfe0bb83">CRYPT_TRUST_REG_ENTRY</a>



<a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a>
 

 

