---
UID: NS:wintrust._CRYPT_REGISTER_ACTIONID
title: "_CRYPT_REGISTER_ACTIONID"
author: windows-sdk-content
description: Provides information about the functions of a provider.
old-location: security\crypt_register_actionid.htm
tech.root: seccrypto
ms.assetid: 0b2b482f-f087-4be7-b17f-91c287c3460d
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCRYPT_REGISTER_ACTIONID, CRYPT_REGISTER_ACTIONID, CRYPT_REGISTER_ACTIONID structure [Security], PCRYPT_REGISTER_ACTIONID, PCRYPT_REGISTER_ACTIONID structure pointer [Security], _CRYPT_REGISTER_ACTIONID, security.crypt_register_actionid, wintrust/CRYPT_REGISTER_ACTIONID, wintrust/PCRYPT_REGISTER_ACTIONID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
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
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_REGISTER_ACTIONID
product: Windows
targetos: Windows
req.typenames: CRYPT_REGISTER_ACTIONID, *PCRYPT_REGISTER_ACTIONID
req.redist: 
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
 

 

