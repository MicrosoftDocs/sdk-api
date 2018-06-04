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

# MsiSummaryInfoGetPropertyCount function


## -description


The 
<b>MsiSummaryInfoGetPropertyCount</b> function returns the number of existing properties in the summary information stream.


## -parameters




### -param hSummaryInfo [in]

Handle to summary information.


### -param puiPropertyCount [out]

Location to receive the total property count.


## -returns



This function returns UINT.




## -see-also




<a href="database_functions.htm">Summary Information Property Functions</a>



<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>
 

 

