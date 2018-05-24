---
UID: NF:credentialprovider.ICredentialProvider.Advise
title: ICredentialProvider::Advise
author: windows-driver-content
description: Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.
old-location: shell\ICredentialProvider_Advise.htm
old-project: shell
ms.assetid: 5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],Advise method, ICredentialProvider.Advise, ICredentialProvider::Advise, credentialprovider/ICredentialProvider::Advise, shell.ICredentialProvider_Advise, shell_ICredentialProvider_Advise
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Credentialprovider.h
api_name:
-	ICredentialProvider.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProvider::Advise


## -description


Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.


## -parameters




### -param pcpe [in]

Type: <b><a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> callback interface to be used as the notification mechanism.


### -param upAdviseContext [in]

Type: <b>UINT_PTR</b>

A pointer to an integer that uniquely identifies which credential provider has requested re-enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method does not need to be implemented, and should return <b>E_NOTIMPL</b> if it doesn't. There might be no reason to call it, such as if the Logon UI or Credential UI never changes or updates.

This method enables the Logon UI and the Credential UI to pass an <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> pointer to the credential provider. This enables the credential provider to have asynchronous callback communication with the Logon or Credential UI. For example, a smart card provider might want to enumerate credentials again when a new smart card is inserted. In order to trigger the Logon UI to get credentials again,  the credential provider should call <a href="https://msdn.microsoft.com/bff835ed-01b9-4620-a97c-c64a2445e02a">CredentialsChanged</a> providing the <i>upAdviseContext</i> identifier.

Credential providers that implement this method have the responsibility of calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the provided <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a>. Those credential providers also need to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> during the <a href="https://msdn.microsoft.com/d971c7be-f440-41ce-945d-4dbe51554e59">UnAdvise</a> method.




## -see-also




<a href="https://msdn.microsoft.com/7ce6cd61-16d1-414e-b9b3-4929a65c0cc6">ICredentialProvider</a>



<a href="https://msdn.microsoft.com/d971c7be-f440-41ce-945d-4dbe51554e59">ICredentialProvider::UnAdvise</a>
 

 

