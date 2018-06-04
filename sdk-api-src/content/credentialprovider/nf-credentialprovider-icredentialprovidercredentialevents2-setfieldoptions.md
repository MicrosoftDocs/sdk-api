---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

