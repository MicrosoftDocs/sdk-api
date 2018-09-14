---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.AppendFieldComboBoxItem
title: ICredentialProviderCredentialEvents::AppendFieldComboBoxItem
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_AppendFieldComboBoxItem.htm
tech.root: shell
ms.assetid: 3d434b2c-29be-4301-9271-89688ec8d048
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: AppendFieldComboBoxItem, AppendFieldComboBoxItem method [Windows Shell], AppendFieldComboBoxItem method [Windows Shell],ICredentialProviderCredentialEvents interface, ICredentialProviderCredentialEvents interface [Windows Shell],AppendFieldComboBoxItem method, ICredentialProviderCredentialEvents.AppendFieldComboBoxItem, ICredentialProviderCredentialEvents::AppendFieldComboBoxItem, _shell_ICredentialProviderCredentialEvents_AppendFieldComboBoxItem, credentialprovider/ICredentialProviderCredentialEvents::AppendFieldComboBoxItem, shell.ICredentialProviderCredentialEvents_AppendFieldComboBoxItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICredentialProviderCredentialEvents.AppendFieldComboBoxItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::AppendFieldComboBoxItem


## -description


Communicates to the Logon UI or Credential UI that a combo box needs an item appended and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>

The credential containing the combo box that needs an item added. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the combo box.


### -param pszItem [in]

Type: <b>LPCWSTR</b>

The string that will be appended to the combo box as a new option.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



