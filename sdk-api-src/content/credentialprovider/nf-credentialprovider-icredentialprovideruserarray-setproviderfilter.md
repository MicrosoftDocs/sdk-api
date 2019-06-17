---
UID: NF:credentialprovider.ICredentialProviderUserArray.SetProviderFilter
title: ICredentialProviderUserArray::SetProviderFilter (credentialprovider.h)
author: windows-sdk-content
description: Limits the set of users in the array to either local accounts or Microsoft accounts.
old-location: shell\ICredentialProviderUserArray_SetProviderFilter.htm
tech.root: shell
ms.assetid: 86FC48BF-FEEA-40c4-91CA-21FFAC210CFA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICredentialProviderUserArray interface [Windows Shell],SetProviderFilter method, ICredentialProviderUserArray.SetProviderFilter, ICredentialProviderUserArray::SetProviderFilter, SetProviderFilter, SetProviderFilter method [Windows Shell], SetProviderFilter method [Windows Shell],ICredentialProviderUserArray interface, credentialprovider/ICredentialProviderUserArray::SetProviderFilter, shell.ICredentialProviderUserArray_SetProviderFilter
ms.topic: method
f1_keywords: ["credentialprovider/ICredentialProviderUserArray.SetProviderFilter"]
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
 - ICredentialProviderUserArray.SetProviderFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderUserArray::SetProviderFilter


## -description


Limits the set of users in the array to either local accounts or Microsoft accounts.


## -parameters




### -param guidProviderToFilterTo [in]

Set this parameter to Identity_LocalUserProvider for the local accounts credential provider; otherwise set it to the GUID of the Microsoft account provider.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a> object contains all of the available users in the current <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/ne-credentialprovider-_credential_provider_usage_scenario">scenario</a>. This method enables your credential provider to specify a particular subset of those users. For example, if your credential provider handles only Microsoft account users from a specific connected provider, it can call this method with the Microsoft account provider's ID to filter out users that belong to other providers.

This method can only be called once, to filter for a single account provider. If the method is called again, the call will fail with a return value of E_UNEXPECTED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getproviderid">ICredentialProviderUser::GetProviderID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>
 

 

