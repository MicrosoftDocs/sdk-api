---
UID: NF:credentialprovider.ICredentialProviderCredential.CommandLinkClicked
title: ICredentialProviderCredential::CommandLinkClicked
author: windows-driver-content
description: Enables the Logon UI and Credential UI to indicate that a link was clicked.
old-location: shell\ICredentialProviderCredential_CommandLinkClicked.htm
old-project: shell
ms.assetid: 04e371cb-f968-4a15-9285-e676dff59899
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CommandLinkClicked, CommandLinkClicked method [Windows Shell], CommandLinkClicked method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],CommandLinkClicked method, ICredentialProviderCredential.CommandLinkClicked, ICredentialProviderCredential::CommandLinkClicked, _shell_ICredentialProviderCredential_CommandLinkClicked, credentialprovider/ICredentialProviderCredential::CommandLinkClicked, shell.ICredentialProviderCredential_CommandLinkClicked
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
-	ICredentialProviderCredential.CommandLinkClicked
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredential::CommandLinkClicked


## -description


Enables the Logon UI and Credential UI to indicate that a link was clicked.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field clicked on.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method contains the logic that the credential provider uses to respond to the click.



