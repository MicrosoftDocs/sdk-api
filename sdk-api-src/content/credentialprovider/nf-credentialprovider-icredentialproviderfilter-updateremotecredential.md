---
UID: NF:credentialprovider.ICredentialProviderFilter.UpdateRemoteCredential
title: ICredentialProviderFilter::UpdateRemoteCredential (credentialprovider.h)
description: Updates a credential from a remote session.
helpviewer_keywords: ["ICredentialProviderFilter interface [Windows Shell]","UpdateRemoteCredential method","ICredentialProviderFilter.UpdateRemoteCredential","ICredentialProviderFilter::UpdateRemoteCredential","UpdateRemoteCredential","UpdateRemoteCredential method [Windows Shell]","UpdateRemoteCredential method [Windows Shell]","ICredentialProviderFilter interface","_shell_ICredentialProviderFilter_UpdateRemoteCredential","credentialprovider/ICredentialProviderFilter::UpdateRemoteCredential","shell.ICredentialProviderFilter_UpdateRemoteCredential"]
old-location: shell\ICredentialProviderFilter_UpdateRemoteCredential.htm
tech.root: shell
ms.assetid: d0730f67-e4f1-42b2-823a-75b08a5c952e
ms.date: 12/05/2018
ms.keywords: ICredentialProviderFilter interface [Windows Shell],UpdateRemoteCredential method, ICredentialProviderFilter.UpdateRemoteCredential, ICredentialProviderFilter::UpdateRemoteCredential, UpdateRemoteCredential, UpdateRemoteCredential method [Windows Shell], UpdateRemoteCredential method [Windows Shell],ICredentialProviderFilter interface, _shell_ICredentialProviderFilter_UpdateRemoteCredential, credentialprovider/ICredentialProviderFilter::UpdateRemoteCredential, shell.ICredentialProviderFilter_UpdateRemoteCredential
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderFilter::UpdateRemoteCredential
 - credentialprovider/ICredentialProviderFilter::UpdateRemoteCredential
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderFilter.UpdateRemoteCredential
---

# ICredentialProviderFilter::UpdateRemoteCredential


## -description

Updates a credential from a remote session.

## -parameters

### -param pcpcsIn [in]

Type: <b>const <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A constant pointer to a <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.

### -param pcpcsOut [out]

Type: <b><a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to a <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

