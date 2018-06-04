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

# _MFNetCredentialManagerGetParam structure


## -description



Contains the authentication information for the credential manager.




## -struct-fields




### -field hrOp

The response code of the authentication challenge. For example, NS_E_PROXY_ACCESSDENIED.


### -field fAllowLoggedOnUser

Set this flag to <b>TRUE</b> if the currently logged on user's credentials should be used as the default credentials.


### -field fClearTextPackage

If <b>TRUE</b>, the authentication package will send unencrypted credentials over the network. Otherwise, the authentication package encrypts the credentials.


### -field pszUrl

The original URL that requires authentication.


### -field pszSite

The name of the site or proxy that requires authentication.


### -field pszRealm

The name of the realm for this authentication.


### -field pszPackage

The name of the authentication package. For example, "Digest" or "MBS_BASIC".


### -field nRetries

The number of times that the credential manager should retry after authentication fails.


## -see-also




<a href="https://msdn.microsoft.com/ff11ff99-18bf-4c4c-93fd-31c06309f105">IMFNetCredentialManager::BeginGetCredentials</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

