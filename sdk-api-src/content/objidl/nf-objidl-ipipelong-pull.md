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

# IPipeLong::Pull


## -description


Retrieves data of the long integer type from the pipe source.


## -parameters




### -param buf [out]

A pointer to the memory buffer that receives the data. The buffer must be able to hold at least the number of long integers specified in <i>cRequest</i>.


### -param cRequest [in]

The number of long integers requested.


### -param pcReturned [out]

The actual number of long integers returned.


## -returns



This method returns S_OK to indicate that the data was retrieved successfully.




## -remarks



When the <b>Pull</b> method is called, data is requested from the provider of the pipe. The caller must provide a buffer that will hold at least the number of long integers specified in the <i>cRequest</i> parameter. The proxy will unmarshal the data into the provided buffer and set the number of long integers actually provided in <i>pcReturned</i>. The <i>pcReturned</i> parameter can be less than or equal to <i>cRequest</i>, but it will never be greater. When <i>pcReturned</i> is 0, it indicates that there is no more data.




## -see-also




<a href="https://msdn.microsoft.com/c1b4d3b3-e1bf-4441-8cea-b667b82c4c27">IPipeLong</a>
 

 

