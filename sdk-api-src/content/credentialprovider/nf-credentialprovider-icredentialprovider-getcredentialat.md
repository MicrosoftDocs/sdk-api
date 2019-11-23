---
UID: NF:credentialprovider.ICredentialProvider.GetCredentialAt
title: ICredentialProvider::GetCredentialAt (credentialprovider.h)

description: Gets a specific credential.
old-location: shell\ICredentialProvider_GetCredentialAt.htm
tech.root: shell
ms.assetid: eec370b7-0db8-492f-8dc3-4f391e1a55e7

ms.date: 12/05/2018
ms.keywords: GetCredentialAt, GetCredentialAt method [Windows Shell], GetCredentialAt method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetCredentialAt method, ICredentialProvider.GetCredentialAt, ICredentialProvider::GetCredentialAt, credentialprovider/ICredentialProvider::GetCredentialAt, shell.ICredentialProvider_GetCredentialAt, shell_ICredentialProvider_GetCredentialAt
ms.topic: method
f1_keywords: 
 - "credentialprovider/ICredentialProvider.GetCredentialAt"
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
 - ICredentialProvider.GetCredentialAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProvider::GetCredentialAt


## -description


Gets a specific credential.


## -parameters




### -param dwIndex [in]

Type: <b>DWORD</b>

The zero-based index of the credential within the set of credentials enumerated for this credential provider.


### -param ppcpc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>**</b>

The address of a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> instance representing the credential.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

The number of available credentials is retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-getcredentialcount">ICredentialProvider::GetCredentialCount</a>. This method is used by the Logon UI or Credential UI in conjunction with <b>GetCredentialCount</b> to enumerate the credentials.



