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

# ICredentialProviderCredentialWithFieldOptions::GetFieldOptions


## -description


Retrieves the current option set for a specified field in a logon or credential UI. Called by the credential provider framework.


## -parameters




### -param fieldID [in]

The ID of the field in the logon or credential UI.


### -param options [out]

A pointer to an <a href="https://msdn.microsoft.com/6E8623D0-7FC3-4ccb-B17A-CB12A0508F15">CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</a> value that, when this method returns successfully, receives one or more flags that specify the current options for the field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5507E8DE-5746-4031-900B-3EF5C97BC2EE">ICredentialProviderCredentialEvents2::SetFieldOptions</a>



<a href="https://msdn.microsoft.com/37C391D7-23C2-4053-BC7F-62F8AFD50DA3">ICredentialProviderCredentialWithFieldOptions</a>
 

 

