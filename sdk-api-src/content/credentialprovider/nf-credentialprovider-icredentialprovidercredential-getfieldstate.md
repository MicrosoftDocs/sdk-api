---
UID: NF:credentialprovider.ICredentialProviderCredential.GetFieldState
title: ICredentialProviderCredential::GetFieldState (credentialprovider.h)
description: Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile.
helpviewer_keywords: ["GetFieldState","GetFieldState method [Windows Shell]","GetFieldState method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetFieldState method","ICredentialProviderCredential.GetFieldState","ICredentialProviderCredential::GetFieldState","_shell_ICredentialProviderCredential_GetFieldState","credentialprovider/ICredentialProviderCredential::GetFieldState","shell.ICredentialProviderCredential_GetFieldState"]
old-location: shell\ICredentialProviderCredential_GetFieldState.htm
tech.root: shell
ms.assetid: 9a709835-cf89-464d-a257-d16a1312ab44
ms.date: 12/05/2018
ms.keywords: GetFieldState, GetFieldState method [Windows Shell], GetFieldState method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetFieldState method, ICredentialProviderCredential.GetFieldState, ICredentialProviderCredential::GetFieldState, _shell_ICredentialProviderCredential_GetFieldState, credentialprovider/ICredentialProviderCredential::GetFieldState, shell.ICredentialProviderCredential_GetFieldState
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
 - ICredentialProviderCredential::GetFieldState
 - credentialprovider/ICredentialProviderCredential::GetFieldState
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
 - ICredentialProviderCredential.GetFieldState
---

# ICredentialProviderCredential::GetFieldState


## -description

Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field.

### -param pcpfs [out]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_state">CREDENTIAL_PROVIDER_FIELD_STATE</a>*</b>

A pointer to the credential provider field state. This indicates when the field should be displayed on the user tile.

### -param pcpfis [out]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state">CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</a>*</b>

A pointer to the credential provider field interactive state. This indicates when the user can interact with the field.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

