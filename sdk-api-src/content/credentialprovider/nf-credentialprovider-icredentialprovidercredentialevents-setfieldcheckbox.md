---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldCheckbox
title: ICredentialProviderCredentialEvents::SetFieldCheckbox (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldCheckbox method","ICredentialProviderCredentialEvents.SetFieldCheckbox","ICredentialProviderCredentialEvents::SetFieldCheckbox","SetFieldCheckbox","SetFieldCheckbox method [Windows Shell]","SetFieldCheckbox method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldCheckbox","credentialprovider/ICredentialProviderCredentialEvents::SetFieldCheckbox","shell.ICredentialProviderCredentialEvents_SetFieldCheckbox"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldCheckbox.htm
tech.root: shell
ms.assetid: a2d5e08f-6a23-4633-beef-8507ab66b102
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldCheckbox method, ICredentialProviderCredentialEvents.SetFieldCheckbox, ICredentialProviderCredentialEvents::SetFieldCheckbox, SetFieldCheckbox, SetFieldCheckbox method [Windows Shell], SetFieldCheckbox method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldCheckbox, credentialprovider/ICredentialProviderCredentialEvents::SetFieldCheckbox, shell.ICredentialProviderCredentialEvents_SetFieldCheckbox
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
 - ICredentialProviderCredentialEvents::SetFieldCheckbox
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldCheckbox
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
 - ICredentialProviderCredentialEvents.SetFieldCheckbox
---

# ICredentialProviderCredentialEvents::SetFieldCheckbox


## -description

Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing the checkbox field that is being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique field ID for the checkbox.

### -param bChecked [in]

Type: <b>BOOL</b>

The new state of the checkbox. <b>TRUE</b> indicates the checkbox should be checked, <b>FALSE</b> indicates it should not.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

The new string for the checkbox label.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.