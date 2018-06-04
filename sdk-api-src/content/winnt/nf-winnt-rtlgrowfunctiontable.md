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

# RtlGrowFunctionTable function


## -description


Reports that a dynamic function table has increased in size. 


## -parameters




### -param DynamicTable

An opaque reference returned by <a href="https://msdn.microsoft.com/84ba7171-a4eb-4807-9883-f4fac6296ed0">RtlAddGrowableFunctionTable.</a>.


### -param NewEntryCount [in]

The new number of entries in the <a href="http://msdn.microsoft.com/en-us/library/ft9x1kdx">RUNTIME_FUNCTION</a> array. This must be greater than the previously reported size of the array.


## -returns



This function does not return a value.




## -remarks



<b>RtlGrowFunctionTable</b> should be called after populating the corresponding entries in the <a href="http://msdn.microsoft.com/en-us/library/ft9x1kdx">RUNTIME_FUNCTION</a> array specified in <a href="https://msdn.microsoft.com/84ba7171-a4eb-4807-9883-f4fac6296ed0">RtlAddGrowableFunctionTable.</a>




