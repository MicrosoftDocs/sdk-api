---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldSubmitButton
title: ICredentialProviderCredentialEvents::SetFieldSubmitButton (credentialprovider.h)
description: Enables credentials to set the field that the submit button appears adjacent to.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldSubmitButton method","ICredentialProviderCredentialEvents.SetFieldSubmitButton","ICredentialProviderCredentialEvents::SetFieldSubmitButton","SetFieldSubmitButton","SetFieldSubmitButton method [Windows Shell]","SetFieldSubmitButton method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldSubmitButton","credentialprovider/ICredentialProviderCredentialEvents::SetFieldSubmitButton","shell.ICredentialProviderCredentialEvents_SetFieldSubmitButton"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldSubmitButton.htm
tech.root: shell
ms.assetid: a39d67d7-b34d-482b-bfe1-db1f9cdc8d30
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldSubmitButton method, ICredentialProviderCredentialEvents.SetFieldSubmitButton, ICredentialProviderCredentialEvents::SetFieldSubmitButton, SetFieldSubmitButton, SetFieldSubmitButton method [Windows Shell], SetFieldSubmitButton method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldSubmitButton, credentialprovider/ICredentialProviderCredentialEvents::SetFieldSubmitButton, shell.ICredentialProviderCredentialEvents_SetFieldSubmitButton
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
 - ICredentialProviderCredentialEvents::SetFieldSubmitButton
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldSubmitButton
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
 - ICredentialProviderCredentialEvents.SetFieldSubmitButton
---

# ICredentialProviderCredentialEvents::SetFieldSubmitButton


## -description

Enables credentials to set the field that the submit button appears adjacent to.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential whose submit button location is being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique field ID of the submit button.

### -param dwAdjacentTo [in]

Type: <b>DWORD</b>

The unique field ID of the field that the submit button should be adjacent to when this method completes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.