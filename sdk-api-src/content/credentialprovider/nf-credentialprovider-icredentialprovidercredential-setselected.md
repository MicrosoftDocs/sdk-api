---
UID: NF:credentialprovider.ICredentialProviderCredential.SetSelected
title: ICredentialProviderCredential::SetSelected (credentialprovider.h)
description: Called when a credential is selected. Enables the implementer to set logon characteristics.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","SetSelected method","ICredentialProviderCredential.SetSelected","ICredentialProviderCredential::SetSelected","SetSelected","SetSelected method [Windows Shell]","SetSelected method [Windows Shell]","ICredentialProviderCredential interface","_shell_ICredentialProviderCredential_SetSelected","credentialprovider/ICredentialProviderCredential::SetSelected","shell.ICredentialProviderCredential_SetSelected"]
old-location: shell\ICredentialProviderCredential_SetSelected.htm
tech.root: shell
ms.assetid: 06a0482c-100c-445f-9a77-279d85492f42
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetSelected method, ICredentialProviderCredential.SetSelected, ICredentialProviderCredential::SetSelected, SetSelected, SetSelected method [Windows Shell], SetSelected method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetSelected, credentialprovider/ICredentialProviderCredential::SetSelected, shell.ICredentialProviderCredential_SetSelected
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
 - ICredentialProviderCredential::SetSelected
 - credentialprovider/ICredentialProviderCredential::SetSelected
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
 - ICredentialProviderCredential.SetSelected
---

# ICredentialProviderCredential::SetSelected


## -description

Called when a credential is selected. Enables the implementer to set logon characteristics.

## -parameters

### -param pbAutoLogon [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if selection of the credential indicates that it should attempt to logon immediately and automatically, otherwise <b>FALSE</b>. For example, a credential provider that enumerates an account without a password may want to return this as true.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Returning any value other than <b>S_OK</b> causes the Logon UI and Credential UI to behave as if no selection occurred.

In Windows 10, if a credential provider wants to automatically log the user on in a situation Windows does not think is appropriate, the system will display a sign in button as a speed bump. One example of this is when a user with an empty password locks the computer or signs out. In that scenario,  Windows does not directly log the user back in.

