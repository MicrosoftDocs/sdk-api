---
UID: NF:credentialprovider.ICredentialProviderEvents.CredentialsChanged
title: ICredentialProviderEvents::CredentialsChanged
author: windows-sdk-content
description: Signals the Logon UI or Credential UI that the enumerated list of credentials has changed.
old-location: shell\ICredentialProviderEvents_CredentialsChanged.htm
tech.root: shell
ms.assetid: bff835ed-01b9-4620-a97c-c64a2445e02a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CredentialsChanged, CredentialsChanged method [Windows Shell], CredentialsChanged method [Windows Shell],ICredentialProviderEvents interface, ICredentialProviderEvents interface [Windows Shell],CredentialsChanged method, ICredentialProviderEvents.CredentialsChanged, ICredentialProviderEvents::CredentialsChanged, credentialprovider/ICredentialProviderEvents::CredentialsChanged, shell.ICredentialProviderEvents_CredentialsChanged, shell_ICredentialProviderEvents_CredentialsChanged
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
 - ICredentialProviderEvents.CredentialsChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderEvents::CredentialsChanged


## -description


Signals the Logon UI or Credential UI that the enumerated list of credentials has changed. This happens when the number of credentials change, the individual credentials change, or the number of fields available change. This is an asynchronous method.


## -parameters




### -param upAdviseContext [in]

Type: <b>UINT_PTR</b>

A pointer to an integer that uniquely identifies which credential provider has requested re-enumeration. The credential provider should pass back the interface pointer it received from <a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a> in this parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the past, many credential providers used <b>ICredentialProviderEvents::CredentialsChanged</b> to update UI. While this works, it causes a re-enumeration of all the credentials from the calling credential provider. The processing of this event can, under some circumstances, lead to flashing or focus changes in the UI due to this re-enumeration. Therefore, using <b>ICredentialProviderEvents::CredentialsChanged</b> solely for UI updates is discouraged. The new recommendation is as follows:

                

<ul>
<li>Use <b>ICredentialProviderEvents::CredentialsChanged</b> only if a credential provider needs to do an auto logon or change the number of credentials it is enumerating.</li>
<li>Use <a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a> to update a credential provider's Logon UI or Credential UI.</li>
</ul>


