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

# IWMWriter::Flush


## -description



The functionality of the <b>Flush</b> method has been removed, because <a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">IWMWriter::EndWriting</a> performs the needed checks internally. For compatibility with older applications, calls to flush will always return S_OK even though the call does nothing.




## -parameters






## -returns



This method always returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>
 

 

