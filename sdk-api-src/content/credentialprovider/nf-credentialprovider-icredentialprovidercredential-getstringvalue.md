---
UID: NF:credentialprovider.ICredentialProviderCredential.GetStringValue
title: ICredentialProviderCredential::GetStringValue (credentialprovider.h)
description: Enables retrieval of text from a credential with a text field.
helpviewer_keywords: ["GetStringValue","GetStringValue method [Windows Shell]","GetStringValue method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetStringValue method","ICredentialProviderCredential.GetStringValue","ICredentialProviderCredential::GetStringValue","credentialprovider/ICredentialProviderCredential::GetStringValue","shell.ICredentialProviderCredential_GetStringValue","shell_ICredentialProviderCredential_GetStringValue"]
old-location: shell\ICredentialProviderCredential_GetStringValue.htm
tech.root: shell
ms.assetid: b891c735-9822-4bc1-a1cc-0c50b35c03c4
ms.date: 12/05/2018
ms.keywords: GetStringValue, GetStringValue method [Windows Shell], GetStringValue method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetStringValue method, ICredentialProviderCredential.GetStringValue, ICredentialProviderCredential::GetStringValue, credentialprovider/ICredentialProviderCredential::GetStringValue, shell.ICredentialProviderCredential_GetStringValue, shell_ICredentialProviderCredential_GetStringValue
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
 - ICredentialProviderCredential::GetStringValue
 - credentialprovider/ICredentialProviderCredential::GetStringValue
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
 - ICredentialProviderCredential.GetStringValue
---

# ICredentialProviderCredential::GetStringValue


## -description

Enables retrieval of text from a credential with a text field.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field.

### -param ppsz [out]

Type: <b>LPWSTR*</b>

A pointer to the memory containing a null-terminated Unicode string to return to the Logon UI or Credential UI.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is optional.

The Logon UI and Credential UI us this method to obtain the <i>pszLabel</i> for a field. This information is necessary to get values for <b>CPFT_LARGE_TEXT</b>, <b>CPFT_SMALL_TEXT</b>, <b>CPFT_COMMAND_LINK</b>, <b>CPFT_EDIT_TEXT</b>, and <b>CPFT_PASSWORD_TEXT</b> fields.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>