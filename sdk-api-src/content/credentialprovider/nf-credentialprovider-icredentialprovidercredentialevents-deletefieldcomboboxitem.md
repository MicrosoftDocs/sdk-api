---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem
title: ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem.htm
old-project: shell
ms.assetid: 1d871480-4424-4a5b-8650-0211bad8b09a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DeleteFieldComboBoxItem, DeleteFieldComboBoxItem method [Windows Shell], DeleteFieldComboBoxItem method [Windows Shell],ICredentialProviderCredentialEvents interface, ICredentialProviderCredentialEvents interface [Windows Shell],DeleteFieldComboBoxItem method, ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem, ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem, _shell_ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem, credentialprovider/ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem, shell.ICredentialProviderCredentialEvents_DeleteFieldComboBoxItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Credentialprovider.h
api_name:
-	ICredentialProviderCredentialEvents.DeleteFieldComboBoxItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredentialEvents::DeleteFieldComboBoxItem


## -description


Communicates to the Logon UI or Credential UI that an item should be deleted from a combo box and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>


                        The credential containing the combo box that needs to be updated. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the combo box.


### -param dwItem [in]

Type: <b>DWORD</b>

The index of the item that is deleted.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



