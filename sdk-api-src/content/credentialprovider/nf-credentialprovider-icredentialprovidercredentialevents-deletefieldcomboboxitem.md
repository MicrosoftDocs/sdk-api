---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem
title: ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem.htm
tech.root: shell
ms.assetid: 1d871480-4424-4a5b-8650-0211bad8b09a
ms.date: 12/05/2018
ms.keywords: DeleteFieldComboBoxItem, DeleteFieldComboBoxItem method [Windows Shell], DeleteFieldComboBoxItem method [Windows Shell],ICredentialProviderCredentialEvents interface, ICredentialProviderCredentialEvents interface [Windows Shell],DeleteFieldComboBoxItem method, ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem, ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem, _shell_ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem, credentialprovider/ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem, shell.ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem
f1_keywords:
- credentialprovider/ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Credentialprovider.h
api_name:
- ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem


## -description


Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing the combo box that needs to be updated. This value should be set to <b>this</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the combo box.


### -param dwItem [in]

Type: <b>DWORD</b>

The index of the item that is deleted.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



