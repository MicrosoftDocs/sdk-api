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

# Header_ClearFilter macro


## -description


Clears the filter for a given header control. You can use this macro or send the <a href="https://msdn.microsoft.com/74c0265e-68d1-4414-8fd9-20f5f041d4b4">HDM_CLEARFILTER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

A value specifying the column of the filter to be cleared. Specifying -1 will clear all of the filters. 


## -remarks



If the column value is specified as -1, all the filters will be cleared and the <a href="https://msdn.microsoft.com/0a46af14-569a-4119-881f-549a130f9b0d">HDN_FILTERCHANGE</a> notification will be sent only once. 




## -see-also




<a href="https://msdn.microsoft.com/2b789b52-d083-46ee-b032-fe24771b3193">Header_ClearAllFilters</a>
 

 

