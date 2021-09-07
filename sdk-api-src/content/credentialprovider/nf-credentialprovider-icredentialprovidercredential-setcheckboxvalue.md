---
UID: NF:credentialprovider.ICredentialProviderCredential.SetCheckboxValue
title: ICredentialProviderCredential::SetCheckboxValue (credentialprovider.h)
description: Enables a Logon UI and Credential UI to indicate that a checkbox value has changed.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","SetCheckboxValue method","ICredentialProviderCredential.SetCheckboxValue","ICredentialProviderCredential::SetCheckboxValue","SetCheckboxValue","SetCheckboxValue method [Windows Shell]","SetCheckboxValue method [Windows Shell]","ICredentialProviderCredential interface","_shell_ICredentialProviderCredential_SetCheckboxValue","credentialprovider/ICredentialProviderCredential::SetCheckboxValue","shell.ICredentialProviderCredential_SetCheckboxValue"]
old-location: shell\ICredentialProviderCredential_SetCheckboxValue.htm
tech.root: shell
ms.assetid: 7da8e80f-1cbe-4a10-96a0-7eb6e61b0f9b
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetCheckboxValue method, ICredentialProviderCredential.SetCheckboxValue, ICredentialProviderCredential::SetCheckboxValue, SetCheckboxValue, SetCheckboxValue method [Windows Shell], SetCheckboxValue method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetCheckboxValue, credentialprovider/ICredentialProviderCredential::SetCheckboxValue, shell.ICredentialProviderCredential_SetCheckboxValue
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
 - ICredentialProviderCredential::SetCheckboxValue
 - credentialprovider/ICredentialProviderCredential::SetCheckboxValue
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
 - ICredentialProviderCredential.SetCheckboxValue
---

# ICredentialProviderCredential::SetCheckboxValue


## -description

Enables a Logon UI and Credential UI to indicate that a checkbox value has changed.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field to update.

### -param bChecked [in]

Type: <b>BOOL</b>

Indicates the new value for the checkbox. <b>TRUE</b> means the checkbox should be checked, <b>FALSE</b> means unchecked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

