---
UID: NS:mfidl._MFNetCredentialManagerGetParam
title: MFNetCredentialManagerGetParam (mfidl.h)
author: windows-sdk-content
description: Contains the authentication information for the credential manager.
old-location: mf\mfnetcredentialmanagergetparam.htm
tech.root: medfound
ms.assetid: 951d74df-11f8-4623-a81b-63e632f80d0e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 951d74df-11f8-4623-a81b-63e632f80d0e, MFNetCredentialManagerGetParam, MFNetCredentialManagerGetParam structure [Media Foundation], mf.mfnetcredentialmanagergetparam, mfidl/MFNetCredentialManagerGetParam
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfidl.h
api_name:
 - MFNetCredentialManagerGetParam
product: Windows
targetos: Windows
req.typenames: MFNetCredentialManagerGetParam
req.redist: 
---

# MFNetCredentialManagerGetParam structure


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
 

 

