---
UID: NF:credentialprovider.ICredentialProvider.GetCredentialAt
title: ICredentialProvider::GetCredentialAt
author: windows-sdk-content
description: Gets a specific credential.
old-location: shell\ICredentialProvider_GetCredentialAt.htm
old-project: shell
ms.assetid: eec370b7-0db8-492f-8dc3-4f391e1a55e7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetCredentialAt, GetCredentialAt method [Windows Shell], GetCredentialAt method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetCredentialAt method, ICredentialProvider.GetCredentialAt, ICredentialProvider::GetCredentialAt, credentialprovider/ICredentialProvider::GetCredentialAt, shell.ICredentialProvider_GetCredentialAt, shell_ICredentialProvider_GetCredentialAt
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
 - ICredentialProvider.GetCredentialAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProvider::GetCredentialAt


## -description


Gets a specific credential.


## -parameters




### -param dwIndex [in]

Type: <b>DWORD</b>

The zero-based index of the credential within the set of credentials enumerated for this credential provider.


### -param ppcpc [out]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>**</b>

The address of a pointer to a <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a> instance representing the credential.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

The number of available credentials is retrieved by <a href="https://msdn.microsoft.com/7d940d46-d4c2-4ab5-8559-416d78d3579e">ICredentialProvider::GetCredentialCount</a>. This method is used by the Logon UI or Credential UI in conjunction with <b>GetCredentialCount</b> to enumerate the credentials.



