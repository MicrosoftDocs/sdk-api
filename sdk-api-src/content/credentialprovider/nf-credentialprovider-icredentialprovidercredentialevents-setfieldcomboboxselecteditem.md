---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldComboBoxSelectedItem
title: ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that the selected item in a combo box has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldComboBoxSelectedItem method","ICredentialProviderCredentialEvents.SetFieldComboBoxSelectedItem","ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem","SetFieldComboBoxSelectedItem","SetFieldComboBoxSelectedItem method [Windows Shell]","SetFieldComboBoxSelectedItem method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldComboBoxSelectedItem","credentialprovider/ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem","shell.ICredentialProviderCredentialEvents_SetFieldComboBoxSelectedItem"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldComboBoxSelectedItem.htm
tech.root: shell
ms.assetid: 79d66546-8553-4b70-9fe6-aa1b95c1cf25
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldComboBoxSelectedItem method, ICredentialProviderCredentialEvents.SetFieldComboBoxSelectedItem, ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem, SetFieldComboBoxSelectedItem, SetFieldComboBoxSelectedItem method [Windows Shell], SetFieldComboBoxSelectedItem method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldComboBoxSelectedItem, credentialprovider/ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem, shell.ICredentialProviderCredentialEvents_SetFieldComboBoxSelectedItem
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
 - ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem
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
 - ICredentialProviderCredentialEvents.SetFieldComboBoxSelectedItem
---

# ICredentialProviderCredentialEvents::SetFieldComboBoxSelectedItem


## -description

Communicates to the Logon UI or Credential UI that the selected item in a combo box has changed and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing the combo box being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the combo box.

### -param dwSelectedItem [in]

Type: <b>DWORD</b>

The index of the item to select in the combo box.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.