---
UID: NF:credentialprovider.ICredentialProviderCredential.SetDeselected
title: ICredentialProviderCredential::SetDeselected (credentialprovider.h)
description: Called when a credential loses selection.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","SetDeselected method","ICredentialProviderCredential.SetDeselected","ICredentialProviderCredential::SetDeselected","SetDeselected","SetDeselected method [Windows Shell]","SetDeselected method [Windows Shell]","ICredentialProviderCredential interface","_shell_ICredentialProviderCredential_SetDeselected","credentialprovider/ICredentialProviderCredential::SetDeselected","shell.ICredentialProviderCredential_SetDeselected"]
old-location: shell\ICredentialProviderCredential_SetDeselected.htm
tech.root: shell
ms.assetid: 89c01b7c-0d22-44f8-9934-b01d7410f85f
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetDeselected method, ICredentialProviderCredential.SetDeselected, ICredentialProviderCredential::SetDeselected, SetDeselected, SetDeselected method [Windows Shell], SetDeselected method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetDeselected, credentialprovider/ICredentialProviderCredential::SetDeselected, shell.ICredentialProviderCredential_SetDeselected
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
 - ICredentialProviderCredential::SetDeselected
 - credentialprovider/ICredentialProviderCredential::SetDeselected
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
 - ICredentialProviderCredential.SetDeselected
---

# ICredentialProviderCredential::SetDeselected


## -description

Called when a credential loses selection.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Credential providers should use this method to purge all buffers containing sensitive information such as a password or Personal Identification Number (PIN). This is in addition to purging them in the destructor of the class that stores them.

