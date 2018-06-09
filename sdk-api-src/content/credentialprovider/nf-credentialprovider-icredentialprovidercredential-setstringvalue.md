---
UID: NF:credentialprovider.ICredentialProviderCredential.SetStringValue
title: ICredentialProviderCredential::SetStringValue
author: windows-sdk-content
description: Enables a Logon UI or Credential UI to update the text for a CPFT_EDIT_TEXT fields as the user types in them.
old-location: shell\ICredentialProviderCredential_SetStringValue.htm
old-project: shell
ms.assetid: ea2007b9-fff1-4cd2-8656-61ec050a8e96
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetStringValue method, ICredentialProviderCredential.SetStringValue, ICredentialProviderCredential::SetStringValue, SetStringValue, SetStringValue method [Windows Shell], SetStringValue method [Windows Shell],ICredentialProviderCredential interface, credentialprovider/ICredentialProviderCredential::SetStringValue, shell.ICredentialProviderCredential_SetStringValue, shell_ICredentialProviderCredential_SetStringValue
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
 - ICredentialProviderCredential.SetStringValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredential::SetStringValue


## -description


Enables a Logon UI or Credential UI to update the text for a <b>CPFT_EDIT_TEXT</b> fields as the user types in them.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field that needs to be updated.


### -param psz [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the new text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is optional.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>


