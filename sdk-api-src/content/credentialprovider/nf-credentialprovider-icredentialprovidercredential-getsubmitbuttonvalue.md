---
UID: NF:credentialprovider.ICredentialProviderCredential.GetSubmitButtonValue
title: ICredentialProviderCredential::GetSubmitButtonValue (credentialprovider.h)
description: Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI.
helpviewer_keywords: ["GetSubmitButtonValue","GetSubmitButtonValue method [Windows Shell]","GetSubmitButtonValue method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetSubmitButtonValue method","ICredentialProviderCredential.GetSubmitButtonValue","ICredentialProviderCredential::GetSubmitButtonValue","_shell_ICredentialProviderCredential_GetSubmitButtonValue","credentialprovider/ICredentialProviderCredential::GetSubmitButtonValue","shell.ICredentialProviderCredential_GetSubmitButtonValue"]
old-location: shell\ICredentialProviderCredential_GetSubmitButtonValue.htm
tech.root: shell
ms.assetid: 74adc133-aa4d-405f-a98d-c9cfc719648a
ms.date: 12/05/2018
ms.keywords: GetSubmitButtonValue, GetSubmitButtonValue method [Windows Shell], GetSubmitButtonValue method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetSubmitButtonValue method, ICredentialProviderCredential.GetSubmitButtonValue, ICredentialProviderCredential::GetSubmitButtonValue, _shell_ICredentialProviderCredential_GetSubmitButtonValue, credentialprovider/ICredentialProviderCredential::GetSubmitButtonValue, shell.ICredentialProviderCredential_GetSubmitButtonValue
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
 - ICredentialProviderCredential::GetSubmitButtonValue
 - credentialprovider/ICredentialProviderCredential::GetSubmitButtonValue
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
 - ICredentialProviderCredential.GetSubmitButtonValue
---

# ICredentialProviderCredential::GetSubmitButtonValue


## -description

Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI. The Credential UI does not call this method.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field a submit button value is needed for.

### -param pdwAdjacentTo [out]

Type: <b>DWORD*</b>

A pointer to a value that receives the field ID of the field that the submit button should be placed next to.

<b>Note to implementers:</b> Do not return the field ID of a bitmap in this parameter. It is not good UI design to place the submit button next to a bitmap, and doing so can cause a failure in the Logon UI.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The submit button is not labeled as such; that is simply a generic way to refer to the button you click to submit the credentials. The button normally appears as a circular button that contains an arrow pointing to the right, although this appearance could change in later releases. For more information, see <a href="/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_field_type">CPFT_SUBMIT_BUTTON</a>.

You should not hide the submit button unless your credential provider always performs automatic submission. Otherwise it can be confusing to the users since they will not see a way to submit their credentials.

Call this method when assembling the Logon UI. For example usage, see the Credential Providers samples included in the Windows Software Development Kit (SDK).

.