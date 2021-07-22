---
UID: NF:credentialprovider.ICredentialProviderCredential.SetComboBoxSelectedValue
title: ICredentialProviderCredential::SetComboBoxSelectedValue (credentialprovider.h)
description: Enables a Logon UI and Credential UI to indicate that a combo box value has been selected.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","SetComboBoxSelectedValue method","ICredentialProviderCredential.SetComboBoxSelectedValue","ICredentialProviderCredential::SetComboBoxSelectedValue","SetComboBoxSelectedValue","SetComboBoxSelectedValue method [Windows Shell]","SetComboBoxSelectedValue method [Windows Shell]","ICredentialProviderCredential interface","_shell_ICredentialProviderCredential_SetComboBoxSelectedValue","credentialprovider/ICredentialProviderCredential::SetComboBoxSelectedValue","shell.ICredentialProviderCredential_SetComboBoxSelectedValue"]
old-location: shell\ICredentialProviderCredential_SetComboBoxSelectedValue.htm
tech.root: shell
ms.assetid: fe33500b-ab34-4f28-b244-692e62d6d30c
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetComboBoxSelectedValue method, ICredentialProviderCredential.SetComboBoxSelectedValue, ICredentialProviderCredential::SetComboBoxSelectedValue, SetComboBoxSelectedValue, SetComboBoxSelectedValue method [Windows Shell], SetComboBoxSelectedValue method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetComboBoxSelectedValue, credentialprovider/ICredentialProviderCredential::SetComboBoxSelectedValue, shell.ICredentialProviderCredential_SetComboBoxSelectedValue
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
 - ICredentialProviderCredential::SetComboBoxSelectedValue
 - credentialprovider/ICredentialProviderCredential::SetComboBoxSelectedValue
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
 - ICredentialProviderCredential.SetComboBoxSelectedValue
---

# ICredentialProviderCredential::SetComboBoxSelectedValue


## -description

Enables a Logon UI and Credential UI to indicate that a combo box value has been selected.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the combo box that is affected.

### -param dwSelectedItem [in]

Type: <b>DWORD</b>

The specific item selected.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

