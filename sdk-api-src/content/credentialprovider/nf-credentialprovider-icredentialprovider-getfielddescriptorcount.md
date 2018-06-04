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

# ICredentialProvider::GetFieldDescriptorCount


## -description


Retrieves the count of fields in the needed to display this provider's credentials.


## -parameters




### -param pdwCount [out]

Type: <b>DWORD*</b>

Pointer to the field count.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

The count provided by this method must be valid for the entire usage scenario. This means that you need to include all fields, even those that are hidden or only shown under special circumstances. This value cannot be changed during a usage scenario and can only be changed when a new <a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a> call is made to the provider or the <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> instance forces another enumeration.



