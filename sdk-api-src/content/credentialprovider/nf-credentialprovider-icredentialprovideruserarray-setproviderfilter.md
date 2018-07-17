---
UID: NF:credentialprovider.ICredentialProviderUserArray.SetProviderFilter
title: ICredentialProviderUserArray::SetProviderFilter
author: windows-sdk-content
description: Limits the set of users in the array to either local accounts or Microsoft accounts.
old-location: shell\ICredentialProviderUserArray_SetProviderFilter.htm
old-project: shell
ms.assetid: 86FC48BF-FEEA-40c4-91CA-21FFAC210CFA
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICredentialProviderUserArray interface [Windows Shell],SetProviderFilter method, ICredentialProviderUserArray.SetProviderFilter, ICredentialProviderUserArray::SetProviderFilter, SetProviderFilter, SetProviderFilter method [Windows Shell], SetProviderFilter method [Windows Shell],ICredentialProviderUserArray interface, credentialprovider/ICredentialProviderUserArray::SetProviderFilter, shell.ICredentialProviderUserArray_SetProviderFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
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



The <a href="https://msdn.microsoft.com/50FC43C1-B148-4e42-AB38-3559BD056855">ICredentialProviderUserArray</a> object contains all of the available users in the current <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">scenario</a>. This method enables your credential provider to specify a particular subset of those users. For example, if your credential provider handles only Microsoft account users from a specific connected provider, it can call this method with the Microsoft account provider's ID to filter out users that belong to other providers.

This method can only be called once, to filter for a single account provider. If the method is called again, the call will fail with a return value of E_UNEXPECTED.




## -see-also




<a href="https://msdn.microsoft.com/7BD6C532-0266-4579-96FA-91D0AF7E6C4C">ICredentialProviderUser::GetProviderID</a>



<a href="https://msdn.microsoft.com/50FC43C1-B148-4e42-AB38-3559BD056855">ICredentialProviderUserArray</a>
 

 

