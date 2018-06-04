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

# IStorageProviderPropertyHandler::RetrieveProperties


## -description


Gets the properties managed by the sync engine.


## -parameters




### -param propertiesToRetrieve [in]

The identifier for the properties to retrieve.


### -param propertiesToRetrieveCount [in]

The number of properties to retrieve.


### -param retrievedProperties






#### - **retrievedProperties [out]

A collection of properties.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the file or folder cannot be found, this method should return <b>S_OK</b>, but <i>retrievedProperties</i> should be empty.

Any properties that are not managed by the sync engine should return <b>VT_EMPTY</b> for those properties.




## -see-also




<a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a>
 

 

