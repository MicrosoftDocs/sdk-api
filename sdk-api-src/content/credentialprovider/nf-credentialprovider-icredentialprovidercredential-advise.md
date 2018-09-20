---
UID: NF:credentialprovider.ICredentialProviderCredential.Advise
title: ICredentialProviderCredential::Advise
author: windows-sdk-content
description: Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in ICredentialProviderCredential interface.
old-location: shell\ICredentialProviderCredential_Advise.htm
tech.root: shell
ms.assetid: 26db5ec5-78bf-4d88-90af-c822c8d3ce45
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],Advise method, ICredentialProviderCredential.Advise, ICredentialProviderCredential::Advise, credentialprovider/ICredentialProviderCredential::Advise, shell.ICredentialProviderCredential_Advise, shell_ICredentialProviderCredential_Advise
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
 - ICredentialProviderCredential.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredential::Advise


## -description


Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a> interface.


## -parameters




### -param pcpce [in]

Type: <b><a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> callback interface to be used as the notification mechanism.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is optional. If you do not implement this method, you should just return <b>E_NOTIMPL</b>.

Credential providers that implement this method have the responsibility of calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the provided <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a>. Those credential providers also need to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> during the <a href="https://msdn.microsoft.com/29e01ef4-3186-4f9a-9898-b7424bba2b61">UnAdvise</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>



<a href="https://msdn.microsoft.com/29e01ef4-3186-4f9a-9898-b7424bba2b61">ICredentialProviderCredential::UnAdvise</a>
 

 

