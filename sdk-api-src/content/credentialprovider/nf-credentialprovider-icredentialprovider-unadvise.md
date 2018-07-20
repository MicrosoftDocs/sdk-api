---
UID: NF:credentialprovider.ICredentialProvider.UnAdvise
title: ICredentialProvider::UnAdvise
author: windows-sdk-content
description: Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.
old-location: shell\ICredentialProvider_UnAdvise.htm
old-project: shell
ms.assetid: d971c7be-f440-41ce-945d-4dbe51554e59
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICredentialProvider interface [Windows Shell],UnAdvise method, ICredentialProvider.UnAdvise, ICredentialProvider::UnAdvise, UnAdvise, UnAdvise method [Windows Shell], UnAdvise method [Windows Shell],ICredentialProvider interface, credentialprovider/ICredentialProvider::UnAdvise, shell.ICredentialProvider_UnAdvise, shell_ICredentialProvider_UnAdvise
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
 - ICredentialProvider.UnAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProvider::UnAdvise


## -description


Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not need to be implemented, and should return <b>E_NOTIMPL</b> if it does not. There might be no reason to call it, such as if the Logon UI or Credential UI never changes or updates.

If this method is called, it indicates that the <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> pointer provided in <a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a> is no longer valid. It is the responsibility of the credential provider to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the provided <b>ICredentialProviderEvents</b> pointer during this method.

<div class="alert"><b>Important</b>  <p class="note">You should not use this method to clean up allocated memory for the credential provider. you should do that in the destructor of the credential provider as normal.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7ce6cd61-16d1-414e-b9b3-4929a65c0cc6">ICredentialProvider</a>



<a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">ICredentialProvider::Advise</a>
 

 

