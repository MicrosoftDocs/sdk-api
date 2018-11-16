---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.SetFieldOptions
title: ICredentialProviderCredentialEvents2::SetFieldOptions
author: windows-sdk-content
description: Specifies whether a specified field in the logon or credential UI should display a &#0034;password reveal&#0034; glyph or is expected to receive an e-mail address.
old-location: shell\ICredentialProviderCredentialEvents2_SetFieldOptions.htm
tech.root: shell
ms.assetid: 5507E8DE-5746-4031-900B-3EF5C97BC2EE
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICredentialProviderCredentialEvents2 interface [Windows Shell],SetFieldOptions method, ICredentialProviderCredentialEvents2.SetFieldOptions, ICredentialProviderCredentialEvents2::SetFieldOptions, SetFieldOptions, SetFieldOptions method [Windows Shell], SetFieldOptions method [Windows Shell],ICredentialProviderCredentialEvents2 interface, credentialprovider/ICredentialProviderCredentialEvents2::SetFieldOptions, shell.ICredentialProviderCredentialEvents2_SetFieldOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICredentialProviderCredentialEvents2.SetFieldOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- credentialprovider.h
: 
- ICredentialProviderCredentialEvents2.SetFieldOptions
: 
---

# ICredentialProviderCredentialEvents2::SetFieldOptions


## -description


Specifies whether a specified field in the logon or credential UI should display a "password reveal" glyph or is expected to receive an e-mail address.


## -parameters




### -param credential [in]

An <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a> interface pointer to the credential object.


### -param fieldID [in]

The ID of the field in the logon or credential UI for which this option applies.


### -param options [in]

One or more of the <a href="https://msdn.microsoft.com/6E8623D0-7FC3-4ccb-B17A-CB12A0508F15">CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</a> values, which specify the field options.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2">ICredentialProviderCredential2::BeginFieldUpdates</a>



<a href="https://msdn.microsoft.com/D05A558E-79D9-4063-A714-F54D8EB8BBF8">ICredentialProviderCredential2::EndFieldUpdates</a>



<a href="https://msdn.microsoft.com/47290FF7-1785-4470-B3A9-F35C5028A6FE">ICredentialProviderCredentialEvents2</a>



<a href="https://msdn.microsoft.com/DE5E6F0E-F4FD-43ce-A1EB-F45C04C85239">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>
 

 

