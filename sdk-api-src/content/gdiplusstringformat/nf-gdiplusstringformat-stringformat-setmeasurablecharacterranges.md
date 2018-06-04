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

# StringFormat::SetMeasurableCharacterRanges


## -description


The <b>StringFormat::SetMeasurableCharacterRanges</b> method sets a series of character ranges for this 
			<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object that, when in a string, can be measured by the <a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a> method.


## -parameters




### -param rangeCount [in]

Type: <b>INT</b>

Integer that specifies the number of character ranges in the 
					<i>ranges</i> array. 


### -param ranges [in]

Type: <b>const <a href="https://msdn.microsoft.com/7bb98500-d1cf-422d-b1ff-a7ca4c84560e">CharacterRange</a>*</b>

Pointer to an array of 
					<a href="https://msdn.microsoft.com/7bb98500-d1cf-422d-b1ff-a7ca4c84560e">CharacterRange</a> objects that specify the character ranges to be measured. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/374b89d4-4f6f-4875-a34f-8a6e9ee379ab">StringFormat::GetMeasurableCharacterRangeCount</a>
 

 

