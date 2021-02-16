---
UID: NS:mfidl._MFNetCredentialManagerGetParam
title: MFNetCredentialManagerGetParam (mfidl.h)
description: Contains the authentication information for the credential manager.
helpviewer_keywords: ["951d74df-11f8-4623-a81b-63e632f80d0e","MFNetCredentialManagerGetParam","MFNetCredentialManagerGetParam structure [Media Foundation]","mf.mfnetcredentialmanagergetparam","mfidl/MFNetCredentialManagerGetParam"]
old-location: mf\mfnetcredentialmanagergetparam.htm
tech.root: mf
ms.assetid: 951d74df-11f8-4623-a81b-63e632f80d0e
ms.date: 12/05/2018
ms.keywords: 951d74df-11f8-4623-a81b-63e632f80d0e, MFNetCredentialManagerGetParam, MFNetCredentialManagerGetParam structure [Media Foundation], mf.mfnetcredentialmanagergetparam, mfidl/MFNetCredentialManagerGetParam
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
targetos: Windows
req.typenames: MFNetCredentialManagerGetParam
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFNetCredentialManagerGetParam
 - mfidl/_MFNetCredentialManagerGetParam
 - MFNetCredentialManagerGetParam
 - mfidl/MFNetCredentialManagerGetParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNetCredentialManagerGetParam
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

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials">IMFNetCredentialManager::BeginGetCredentials</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>