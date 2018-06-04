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

# CharacterRange::CharacterRange(INT,INT)


## -description


Creates a <b>CharacterRange::CharacterRange</b> object and initializes the data members to the values specified.


## -parameters




### -param first [in]

Type: <b>INT</b>

Integer that specifies the first position of this range. For example, if 
					<i>first</i> is set to 0, then the first position of this range is position 0 in the string. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of positions in this range. 


## -see-also




<a href="https://msdn.microsoft.com/7bb98500-d1cf-422d-b1ff-a7ca4c84560e">CharacterRange</a>



<a href="https://msdn.microsoft.com/374b89d4-4f6f-4875-a34f-8a6e9ee379ab">GetMeasurableCharacterRangeCount</a>



<a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a>



<a href="https://msdn.microsoft.com/5c49c64f-f705-4b33-974b-34ffb1e43ff5">SetMeasurableCharacterRanges</a>
 

 

