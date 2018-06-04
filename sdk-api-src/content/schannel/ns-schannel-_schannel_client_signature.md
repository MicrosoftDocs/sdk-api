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



