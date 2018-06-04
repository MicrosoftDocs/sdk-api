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

# ICredentialProviderFilter::UpdateRemoteCredential


## -description


Updates a credential from a remote session.


## -parameters




### -param pcpcsIn [in]

Type: <b>const <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A constant pointer to a <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.


### -param pcpcsOut [out]

Type: <b><a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/55ff9be3-490d-4f82-92a0-3551ccbcaade">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



