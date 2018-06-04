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

# PSET_RESOURCE_STATUS_ROUTINE_EX callback function


## -description


Called to update the status of a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. 
    The <b>PSET_RESOURCE_STATUS_ROUTINE_EX</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle

A handle to the resource to be updated. The <i>ResourceHandle</i> parameter should 
       contain the same handle that is used for the <i>ResourceHandle</i> parameter in the 
       <a href="https://msdn.microsoft.com/EA798D15-9458-4F66-8D0E-13DA383552F7">OpenV2</a> entry point for this resource.


### -param ResourceStatus

A pointer to a <a href="https://msdn.microsoft.com/CBEBF870-B413-400C-A485-FD093358FB67">RESOURCE_STATUS_EX</a> structure that 
       contains information about the resource's state.


## -returns



One of 
       the following values of the 
       <a href="https://msdn.microsoft.com/d1b9fd8f-7d49-4396-8f0c-6db8fad5749e">RESOURCE_EXIT_STATE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

