---
UID: NF:credentialprovider.ICredentialProviderCredential.CommandLinkClicked
title: ICredentialProviderCredential::CommandLinkClicked (credentialprovider.h)
description: Enables the Logon UI and Credential UI to indicate that a link was clicked.
helpviewer_keywords: ["CommandLinkClicked","CommandLinkClicked method [Windows Shell]","CommandLinkClicked method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","CommandLinkClicked method","ICredentialProviderCredential.CommandLinkClicked","ICredentialProviderCredential::CommandLinkClicked","_shell_ICredentialProviderCredential_CommandLinkClicked","credentialprovider/ICredentialProviderCredential::CommandLinkClicked","shell.ICredentialProviderCredential_CommandLinkClicked"]
old-location: shell\ICredentialProviderCredential_CommandLinkClicked.htm
tech.root: shell
ms.assetid: 04e371cb-f968-4a15-9285-e676dff59899
ms.date: 12/05/2018
ms.keywords: CommandLinkClicked, CommandLinkClicked method [Windows Shell], CommandLinkClicked method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],CommandLinkClicked method, ICredentialProviderCredential.CommandLinkClicked, ICredentialProviderCredential::CommandLinkClicked, _shell_ICredentialProviderCredential_CommandLinkClicked, credentialprovider/ICredentialProviderCredential::CommandLinkClicked, shell.ICredentialProviderCredential_CommandLinkClicked
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderCredential::CommandLinkClicked
 - credentialprovider/ICredentialProviderCredential::CommandLinkClicked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderCredential.CommandLinkClicked
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method contains the logic that the credential provider uses to respond to the click.

