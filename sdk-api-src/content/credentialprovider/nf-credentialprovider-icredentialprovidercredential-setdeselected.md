---
UID: NF:credentialprovider.ICredentialProviderCredential.SetDeselected
title: ICredentialProviderCredential::SetDeselected
author: windows-sdk-content
description: Called when a credential loses selection.
old-location: shell\ICredentialProviderCredential_SetDeselected.htm
old-project: shell
ms.assetid: 89c01b7c-0d22-44f8-9934-b01d7410f85f
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetDeselected method, ICredentialProviderCredential.SetDeselected, ICredentialProviderCredential::SetDeselected, SetDeselected, SetDeselected method [Windows Shell], SetDeselected method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetDeselected, credentialprovider/ICredentialProviderCredential::SetDeselected, shell.ICredentialProviderCredential_SetDeselected
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderCredential.SetDeselected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredential::SetDeselected


## -description


Called when a credential loses selection.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Credential providers should use this method to purge all buffers containing sensitive information such as a password or Personal Identification Number (PIN). This is in addition to purging them in the destructor of the class that stores them.



