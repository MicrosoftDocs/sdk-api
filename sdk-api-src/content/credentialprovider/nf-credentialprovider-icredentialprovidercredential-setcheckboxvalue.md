---
UID: NF:credentialprovider.ICredentialProviderCredential.SetCheckboxValue
title: ICredentialProviderCredential::SetCheckboxValue
author: windows-sdk-content
description: Enables a Logon UI and Credential UI to indicate that a checkbox value has changed.
old-location: shell\ICredentialProviderCredential_SetCheckboxValue.htm
old-project: shell
ms.assetid: 7da8e80f-1cbe-4a10-96a0-7eb6e61b0f9b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetCheckboxValue method, ICredentialProviderCredential.SetCheckboxValue, ICredentialProviderCredential::SetCheckboxValue, SetCheckboxValue, SetCheckboxValue method [Windows Shell], SetCheckboxValue method [Windows Shell],ICredentialProviderCredential interface, _shell_ICredentialProviderCredential_SetCheckboxValue, credentialprovider/ICredentialProviderCredential::SetCheckboxValue, shell.ICredentialProviderCredential_SetCheckboxValue
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
 - ICredentialProviderCredential.SetCheckboxValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredential::SetCheckboxValue


## -description


Enables a Logon UI and Credential UI to indicate that a checkbox value has changed.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field to update.


### -param bChecked [in]

Type: <b>BOOL</b>

Indicates the new value for the checkbox. <b>TRUE</b> means the checkbox should be checked, <b>FALSE</b> means unchecked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



