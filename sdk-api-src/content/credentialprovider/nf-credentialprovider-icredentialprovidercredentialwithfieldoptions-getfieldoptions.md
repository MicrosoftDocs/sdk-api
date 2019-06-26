---
UID: NF:credentialprovider.ICredentialProviderCredentialWithFieldOptions.GetFieldOptions
title: ICredentialProviderCredentialWithFieldOptions::GetFieldOptions (credentialprovider.h)
author: windows-sdk-content
description: Retrieves the current option set for a specified field in a logon or credential UI. Called by the credential provider framework.
old-location: shell\ICredentialProviderCredentialWithFieldOptions_GetFieldOptions.htm
tech.root: shell
ms.assetid: DE5E6F0E-F4FD-43ce-A1EB-F45C04C85239
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFieldOptions, GetFieldOptions method [Windows Shell], GetFieldOptions method [Windows Shell],ICredentialProviderCredentialWithFieldOptions interface, ICredentialProviderCredentialWithFieldOptions interface [Windows Shell],GetFieldOptions method, ICredentialProviderCredentialWithFieldOptions.GetFieldOptions, ICredentialProviderCredentialWithFieldOptions::GetFieldOptions, credentialprovider/ICredentialProviderCredentialWithFieldOptions::GetFieldOptions, shell.ICredentialProviderCredentialWithFieldOptions_GetFieldOptions
ms.topic: method
f1_keywords: 
 - "credentialprovider/ICredentialProviderCredentialWithFieldOptions.GetFieldOptions"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialWithFieldOptions.GetFieldOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredentialWithFieldOptions::GetFieldOptions


## -description


Retrieves the current option set for a specified field in a logon or credential UI. Called by the credential provider framework.


## -parameters




### -param fieldID [in]

The ID of the field in the logon or credential UI.


### -param options [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_credential_field_options">CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</a> value that, when this method returns successfully, receives one or more flags that specify the current options for the field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredentialEvents2::SetFieldOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions">ICredentialProviderCredentialWithFieldOptions</a>
 

 

