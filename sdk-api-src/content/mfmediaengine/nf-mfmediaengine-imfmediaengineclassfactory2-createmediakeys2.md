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

# IMFMediaEngineClassFactory2::CreateMediaKeys2


## -description


Creates a media keys object based on the specified key system.


## -parameters




### -param keySystem [in]

The media key system.


### -param defaultCdmStorePath [in]

Points to the default file location for the  store Content Decryption Module (CDM) data.


### -param inprivateCdmStorePath [in, optional]

Points to a the inprivate location for the  store Content Decryption Module (CDM) data. Specifying this path allows the CDM to comply with the application’s privacy policy by putting personal information in the file location indicated by this path.


### -param ppKeys [out]

Receives the media keys.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/161CFCBF-BBAE-4590-8545-D916EC1885D8">IMFMediaEngineClassFactory2</a>



<a href="https://msdn.microsoft.com/0689d938-e0be-46d7-bfed-add431331a90">IMFMediaKeys</a>
 

 

