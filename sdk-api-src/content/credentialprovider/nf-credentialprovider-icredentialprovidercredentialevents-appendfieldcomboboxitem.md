---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.AppendFieldComboBoxItem
title: ICredentialProviderCredentialEvents::AppendFieldComboBoxItem (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.
helpviewer_keywords: ["AppendFieldComboBoxItem","AppendFieldComboBoxItem method [Windows Shell]","AppendFieldComboBoxItem method [Windows Shell]","ICredentialProviderCredentialEvents interface","ICredentialProviderCredentialEvents interface [Windows Shell]","AppendFieldComboBoxItem method","ICredentialProviderCredentialEvents.AppendFieldComboBoxItem","ICredentialProviderCredentialEvents::AppendFieldComboBoxItem","_shell_ICredentialProviderCredentialEvents_AppendFieldComboBoxItem","credentialprovider/ICredentialProviderCredentialEvents::AppendFieldComboBoxItem","shell.ICredentialProviderCredentialEvents_AppendFieldComboBoxItem"]
old-location: shell\ICredentialProviderCredentialEvents_AppendFieldComboBoxItem.htm
tech.root: shell
ms.assetid: 3d434b2c-29be-4301-9271-89688ec8d048
ms.date: 12/05/2018
ms.keywords: AppendFieldComboBoxItem, AppendFieldComboBoxItem method [Windows Shell], AppendFieldComboBoxItem method [Windows Shell],ICredentialProviderCredentialEvents interface, ICredentialProviderCredentialEvents interface [Windows Shell],AppendFieldComboBoxItem method, ICredentialProviderCredentialEvents.AppendFieldComboBoxItem, ICredentialProviderCredentialEvents::AppendFieldComboBoxItem, _shell_ICredentialProviderCredentialEvents_AppendFieldComboBoxItem, credentialprovider/ICredentialProviderCredentialEvents::AppendFieldComboBoxItem, shell.ICredentialProviderCredentialEvents_AppendFieldComboBoxItem
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
 - ICredentialProviderCredentialEvents::AppendFieldComboBoxItem
 - credentialprovider/ICredentialProviderCredentialEvents::AppendFieldComboBoxItem
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
 - ICredentialProviderCredentialEvents.AppendFieldComboBoxItem
---

# ICredentialProviderCredentialEvents::AppendFieldComboBoxItem


## -description

Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing the combo box that needs an item added. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the combo box.

### -param pszItem [in]

Type: <b>LPCWSTR</b>

The string that will be appended to the combo box as a new option.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.