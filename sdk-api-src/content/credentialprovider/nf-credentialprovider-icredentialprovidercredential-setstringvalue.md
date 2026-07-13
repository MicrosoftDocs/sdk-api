---
UID: NF:credentialprovider.ICredentialProviderCredential.SetStringValue
title: ICredentialProviderCredential::SetStringValue (credentialprovider.h)
description: Enables a Logon UI or Credential UI to update the text for a CPFT_EDIT_TEXT fields as the user types in them.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","SetStringValue method","ICredentialProviderCredential.SetStringValue","ICredentialProviderCredential::SetStringValue","SetStringValue","SetStringValue method [Windows Shell]","SetStringValue method [Windows Shell]","ICredentialProviderCredential interface","credentialprovider/ICredentialProviderCredential::SetStringValue","shell.ICredentialProviderCredential_SetStringValue","shell_ICredentialProviderCredential_SetStringValue"]
old-location: shell\ICredentialProviderCredential_SetStringValue.htm
tech.root: shell
ms.assetid: ea2007b9-fff1-4cd2-8656-61ec050a8e96
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],SetStringValue method, ICredentialProviderCredential.SetStringValue, ICredentialProviderCredential::SetStringValue, SetStringValue, SetStringValue method [Windows Shell], SetStringValue method [Windows Shell],ICredentialProviderCredential interface, credentialprovider/ICredentialProviderCredential::SetStringValue, shell.ICredentialProviderCredential_SetStringValue, shell_ICredentialProviderCredential_SetStringValue
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
 - ICredentialProviderCredential::SetStringValue
 - credentialprovider/ICredentialProviderCredential::SetStringValue
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
 - ICredentialProviderCredential.SetStringValue
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is optional.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>