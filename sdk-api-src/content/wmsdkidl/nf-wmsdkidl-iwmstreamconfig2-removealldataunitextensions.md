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

# IWMStreamConfig2::RemoveAllDataUnitExtensions


## -description



The <b>RemoveAllDataUnitExtensions</b> method removes all data unit extension systems that are associated with the stream.




## -parameters






## -returns



The method always returns S_OK.




## -remarks



The changes will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/db84a33c-bd83-46cb-a97c-76ddeeb74927">IWMStreamConfig2::AddDataUnitExtension</a>



<a href="https://msdn.microsoft.com/766124f6-b376-421b-b2ee-2c280af3bd16">IWMStreamConfig2::GetDataUnitExtension</a>



<a href="https://msdn.microsoft.com/f9a4ec84-4ea3-4e84-9def-7ca93be0f1ce">IWMStreamConfig2::GetDataUnitExtensionCount</a>
 

 

