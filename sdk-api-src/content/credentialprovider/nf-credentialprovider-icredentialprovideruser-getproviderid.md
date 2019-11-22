---
UID: NF:credentialprovider.ICredentialProviderUser.GetProviderID
title: ICredentialProviderUser::GetProviderID (credentialprovider.h)

description: Retrieves the ID of the account provider for this user.
old-location: shell\ICredentialProviderUser_GetProviderID.htm
tech.root: shell
ms.assetid: 7BD6C532-0266-4579-96FA-91D0AF7E6C4C

ms.date: 12/05/2018
ms.keywords: GetProviderID, GetProviderID method [Windows Shell], GetProviderID method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetProviderID method, ICredentialProviderUser.GetProviderID, ICredentialProviderUser::GetProviderID, credentialprovider/ICredentialProviderUser::GetProviderID, shell.ICredentialProviderUser_GetProviderID
ms.topic: method
f1_keywords: 
 - "credentialprovider/ICredentialProviderUser.GetProviderID"
dev_langs:
 - c++
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUser.GetProviderID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderUser::GetProviderID


## -description


Retrieves the ID of the account provider for this user.


## -parameters




### -param providerID [out]

A pointer to a value that, when this method returns successfully, receives the GUID of the user's account provider.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This GUID applies to both logon and credential UI.

This value can also be retrieved as a <b>PROPVARIANT</b> through <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>
 

 

