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

# AM_QueryRate structure


## -description



The <b>AM_QueryRate</b> structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.




## -struct-fields




### -field lMaxForwardFullFrame

Specifies the maximum forward full-frame rate, as rate x 10000.


### -field lMaxReverseFullFrame

Specifies the maximum reverse full-frame rate, as rate x 10000.


## -remarks



Rate is the inverse of speed. For example, if the playback speed is 2x, the rate is 1/2, so the <b>Rate</b> member is set to 5000. Reverse rates are negative.




## -see-also




<a href="https://msdn.microsoft.com/98808ed4-6d34-437b-9729-9cc805bc81f0">AM_RATE_QueryFullFrameRate Property</a>



<a href="https://msdn.microsoft.com/f88c64ce-af76-49fe-8ebd-029928506243">Rate Change Property Set</a>
 

 

