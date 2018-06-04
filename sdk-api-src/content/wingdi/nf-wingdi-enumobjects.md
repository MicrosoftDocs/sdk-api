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

# EnumObjects function


## -description


The <b>EnumObjects</b> function enumerates the pens or brushes available for the specified device context (DC). This function calls the application-defined callback function once for each available object, supplying data describing that object. <b>EnumObjects</b> continues calling the callback function until the callback function returns zero or until all of the objects have been enumerated.


## -parameters




### -param hdc [in]

A handle to the DC.


### -param nType

TBD


### -param lpFunc

TBD


### -param lParam [in]

A pointer to the application-defined data. The data is passed to the callback function along with the object information.


#### - lpObjectFunc [in]

A pointer to the application-defined callback function. For more information about the callback function, see the <a href="https://msdn.microsoft.com/05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3">EnumObjectsProc</a> function.


#### - nObjectType [in]

The object type. This parameter can be OBJ_BRUSH or OBJ_PEN.


## -returns



If the function succeeds, the return value is the last value returned by the callback function. Its meaning is user-defined.

If the objects cannot be enumerated (for example, there are too many objects), the function returns zero without calling the callback function.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3">EnumObjectsProc</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>
 

 

