---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldState
title: ICredentialProviderCredentialEvents::SetFieldState (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldState method","ICredentialProviderCredentialEvents.SetFieldState","ICredentialProviderCredentialEvents::SetFieldState","SetFieldState","SetFieldState method [Windows Shell]","SetFieldState method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldState","credentialprovider/ICredentialProviderCredentialEvents::SetFieldState","shell.ICredentialProviderCredentialEvents_SetFieldState"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldState.htm
tech.root: shell
ms.assetid: d3498bca-cc31-4a80-9f31-e1e6d020d777
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldState method, ICredentialProviderCredentialEvents.SetFieldState, ICredentialProviderCredentialEvents::SetFieldState, SetFieldState, SetFieldState method [Windows Shell], SetFieldState method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldState, credentialprovider/ICredentialProviderCredentialEvents::SetFieldState, shell.ICredentialProviderCredentialEvents_SetFieldState
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
 - ICredentialProviderCredentialEvents::SetFieldState
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldState
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
 - ICredentialProviderCredentialEvents.SetFieldState
---

# ICredentialProviderCredentialEvents::SetFieldState


## -description

Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing a field whose state is being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field where the change occurred to generate the event.

### -param cpfs [in]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_state">CREDENTIAL_PROVIDER_FIELD_STATE</a></b>

The value from the <a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_state">CREDENTIAL_PROVIDER_FIELD_STATE</a> enumeration that specifies the new field state.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.