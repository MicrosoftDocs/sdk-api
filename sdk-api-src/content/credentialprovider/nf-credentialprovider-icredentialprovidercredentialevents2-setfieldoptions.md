---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.SetFieldOptions
title: ICredentialProviderCredentialEvents2::SetFieldOptions (credentialprovider.h)
description: Specifies whether a specified field in the logon or credential UI should display a &quot;password reveal&quot; glyph or is expected to receive an e-mail address.
helpviewer_keywords: ["ICredentialProviderCredentialEvents2 interface [Windows Shell]","SetFieldOptions method","ICredentialProviderCredentialEvents2.SetFieldOptions","ICredentialProviderCredentialEvents2::SetFieldOptions","SetFieldOptions","SetFieldOptions method [Windows Shell]","SetFieldOptions method [Windows Shell]","ICredentialProviderCredentialEvents2 interface","credentialprovider/ICredentialProviderCredentialEvents2::SetFieldOptions","shell.ICredentialProviderCredentialEvents2_SetFieldOptions"]
old-location: shell\ICredentialProviderCredentialEvents2_SetFieldOptions.htm
tech.root: shell
ms.assetid: 5507E8DE-5746-4031-900B-3EF5C97BC2EE
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents2 interface [Windows Shell],SetFieldOptions method, ICredentialProviderCredentialEvents2.SetFieldOptions, ICredentialProviderCredentialEvents2::SetFieldOptions, SetFieldOptions, SetFieldOptions method [Windows Shell], SetFieldOptions method [Windows Shell],ICredentialProviderCredentialEvents2 interface, credentialprovider/ICredentialProviderCredentialEvents2::SetFieldOptions, shell.ICredentialProviderCredentialEvents2_SetFieldOptions
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
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
 - ICredentialProviderCredentialEvents2::SetFieldOptions
 - credentialprovider/ICredentialProviderCredentialEvents2::SetFieldOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2.SetFieldOptions
---

# ICredentialProviderCredentialEvents2::SetFieldOptions


## -description

Specifies whether a specified field in the logon or credential UI should display a "password reveal" glyph or is expected to receive an e-mail address.

## -parameters

### -param credential [in]

An <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> interface pointer to the credential object.

### -param fieldID [in]

The ID of the field in the logon or credential UI for which this option applies.

### -param options [in]

One or more of the <a href="/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_credential_field_options">CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</a> values, which specify the field options.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates">ICredentialProviderCredential2::BeginFieldUpdates</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-endfieldupdates">ICredentialProviderCredential2::EndFieldUpdates</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialwithfieldoptions-getfieldoptions">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>