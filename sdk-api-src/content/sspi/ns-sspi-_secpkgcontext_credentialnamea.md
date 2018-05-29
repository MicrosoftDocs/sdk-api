---
UID: NS:sspi._SecPkgContext_CredentialNameA
title: "_SecPkgContext_CredentialNameA"
author: windows-sdk-content
description: Specifies the credential name for the security context.
old-location: security\secpkgcontext_credentialname.htm
old-project: SecAuthN
ms.assetid: 55ac5db9-9c55-421d-82f5-bdbc54c5d544
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSecPkgContext_CredentialNameA, PSecPkgContext_CredentialName, PSecPkgContext_CredentialName structure pointer [Security], SecPkgContext_CredentialName, SecPkgContext_CredentialName structure [Security], SecPkgContext_CredentialNameA, _SecPkgContext_CredentialNameA, _SecPkgContext_CredentialNameW, security.secpkgcontext_credentialname, sspi/PSecPkgContext_CredentialName, sspi/SecPkgContext_CredentialName"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
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
req.typenames: SecPkgContext_CredentialNameA, *PSecPkgContext_CredentialNameA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgContext_CredentialName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_CredentialNameA structure


## -description


The <b>SecPkgContext_CredentialName</b> structure specifies the credential name for the  <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

This attribute is not supported by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).


## -struct-fields




### -field CredentialType

Type of credential.


### -field sCredentialName

Pointer to a null-terminated string for the credential name.

