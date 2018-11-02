---
UID: NS:schannel._SCHANNEL_CLIENT_SIGNATURE
title: "_SCHANNEL_CLIENT_SIGNATURE"
author: windows-sdk-content
description: Specifies a client signature when a call to the InitializeSecurityContext (Schannel) function cannot access the private key for a client certificate (in this case, the function returns SEC_I_SIGNATURE_NEEDED).
old-location: security\schannel_client_signature.htm
tech.root: secauthn
ms.assetid: 2549a287-bee3-457b-86e3-3330bf23169a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PSCHANNEL_CLIENT_SIGNATURE, PSCHANNEL_CLIENT_SIGNATURE, PSCHANNEL_CLIENT_SIGNATURE structure pointer [Security], SCHANNEL_CLIENT_SIGNATURE, SCHANNEL_CLIENT_SIGNATURE structure [Security], _SCHANNEL_CLIENT_SIGNATURE, schannel/PSCHANNEL_CLIENT_SIGNATURE, schannel/SCHANNEL_CLIENT_SIGNATURE, security.schannel_client_signature"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: schannel.h
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
 - Schannel.h
api_name:
 - SCHANNEL_CLIENT_SIGNATURE
product: Windows
targetos: Windows
req.typenames: SCHANNEL_CLIENT_SIGNATURE, *PSCHANNEL_CLIENT_SIGNATURE
req.redist: 
---

# _SCHANNEL_CLIENT_SIGNATURE structure


## -description


Specifies a client signature when a call to the <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function cannot access the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> for a client certificate (in this case, the function returns <b>SEC_I_SIGNATURE_NEEDED</b>).


## -struct-fields




### -field cbLength

The size, in bytes, of this structure.


### -field aiHash

The ID of the algorithm used to compute the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate.


### -field cbHash

The size, in bytes, of the <b>HashValue</b> array.


### -field HashValue

An array of byte values that specify the hash of the certificate.


### -field CertThumbprint

An array of byte values that specify the certificate thumbprint.


## -remarks



Add a client signature to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="https://msdn.microsoft.com/5ce13a05-874c-4e1a-9be8-aed98609791e">ApplyControlToken</a> function.



