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

# IPersistTuneXmlUtility2::Serialize


## -description


Serializes a tuning request to an XML tuning request string.


## -parameters




### -param piTuneRequest [in]

Pointer to the <a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequest</a> interface for the tuning request object that is serialized.


### -param pString

Pointer to a buffer that receives the XML tuning request string. The caller is responsible for releasing this memory. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d909d505-2ae9-4488-b4c1-42ca32661bf3">IPersistTuneXmlUtility2</a>



<a href="https://msdn.microsoft.com/a42a001b-210c-4e89-823e-ec1e1fa58f67">IPersistTuneXmlUtility::Deserialize</a>



<a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequest</a>
 

 

