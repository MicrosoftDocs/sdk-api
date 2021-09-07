---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldInteractiveState
title: ICredentialProviderCredentialEvents::SetFieldInteractiveState (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldInteractiveState method","ICredentialProviderCredentialEvents.SetFieldInteractiveState","ICredentialProviderCredentialEvents::SetFieldInteractiveState","SetFieldInteractiveState","SetFieldInteractiveState method [Windows Shell]","SetFieldInteractiveState method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldInteractiveState","credentialprovider/ICredentialProviderCredentialEvents::SetFieldInteractiveState","shell.ICredentialProviderCredentialEvents_SetFieldInteractiveState"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldInteractiveState.htm
tech.root: shell
ms.assetid: 649f0f65-78dd-4232-b471-9a18d1448f1d
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldInteractiveState method, ICredentialProviderCredentialEvents.SetFieldInteractiveState, ICredentialProviderCredentialEvents::SetFieldInteractiveState, SetFieldInteractiveState, SetFieldInteractiveState method [Windows Shell], SetFieldInteractiveState method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldInteractiveState, credentialprovider/ICredentialProviderCredentialEvents::SetFieldInteractiveState, shell.ICredentialProviderCredentialEvents_SetFieldInteractiveState
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
 - ICredentialProviderCredentialEvents::SetFieldInteractiveState
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldInteractiveState
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
 - ICredentialProviderCredentialEvents.SetFieldInteractiveState
---

# ICredentialProviderCredentialEvents::SetFieldInteractiveState


## -description

Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing a field whose interactivity state is being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field.

### -param cpfis [in]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state">CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</a></b>

The new interactive state of the field.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.