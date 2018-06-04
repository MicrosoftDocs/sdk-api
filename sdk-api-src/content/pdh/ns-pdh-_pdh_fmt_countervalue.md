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

# _PDH_FMT_COUNTERVALUE structure


## -description



			The 
<b>PDH_FMT_COUNTERVALUE</b> structure contains the computed value of the counter and its status. 


## -struct-fields




### -field CStatus

Counter status that indicates if the counter value is valid. Check this member before using the data in a calculation or displaying its value. For a list of possible values, see 
<a href="https://msdn.microsoft.com/00ea5521-bc28-4a87-aba9-46c911631503">Checking PDH Interface Return Values</a>.


### -field longValue

The computed counter value as a <b>LONG</b>.


### -field doubleValue

The computed counter value as a <b>DOUBLE</b>.


### -field largeValue

The computed counter value as a <b>LONGLONG</b>.


### -field AnsiStringValue

The computed counter value as a <b>LPCSTR</b>. Not supported.


### -field WideStringValue

The computed counter value as a <b>LPCWSTR</b>. Not supported.


## -remarks



You specify the data type of the computed counter value when you call <a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> or <a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a> to compute the counter's value.




## -see-also




<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>
 

 

