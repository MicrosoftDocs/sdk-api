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

# ICredentialProviderCredential::GetFieldState


## -description


Retrieves the field state. The Logon UI and Credential UI use this to gain information about a field of a credential to display this information in the user tile.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field.


### -param pcpfs [out]

Type: <b><a href="https://msdn.microsoft.com/4cc7858c-483b-4fac-96ba-8962bc362422">CREDENTIAL_PROVIDER_FIELD_STATE</a>*</b>

A pointer to the credential provider field state. This indicates when the field should be displayed on the user tile.


### -param pcpfis [out]

Type: <b><a href="https://msdn.microsoft.com/745ac5f0-fcfe-4f42-ab4c-c933f1d3870b">CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</a>*</b>


          A pointer to the credential provider field interactive state. This indicates when the user can interact with the field.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



