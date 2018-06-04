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

# StringFormat::GetMeasurableCharacterRangeCount


## -description


The <b>StringFormat::GetMeasurableCharacterRangeCount</b> method gets the number of measurable character ranges that are currently set. The character ranges that are set can be measured in a string by using the 
			<a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a> method.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns an integer that indicates the number of character ranges that can be measured by <a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a>.




## -see-also




<a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/5c49c64f-f705-4b33-974b-34ffb1e43ff5">StringFormat::SetMeasurableCharacterRanges</a>
 

 

