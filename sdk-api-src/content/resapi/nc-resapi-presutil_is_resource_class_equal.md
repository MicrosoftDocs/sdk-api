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

# PRESUTIL_IS_RESOURCE_CLASS_EQUAL callback function


## -description


Tests whether the resource class of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> is equal to a specified resource class. The <b>PRESUTIL_IS_RESOURCE_CLASS_EQUAL</b> type defines a pointer to this function.


## -parameters




### -param prci [in]

Pointer to a  <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure describing the resource class.


### -param hResource [in]

Handle to the resource whose class is to be compared to <i>prci</i>.


## -returns



If the resource classes are equal, the function returns <b>TRUE</b>.

If the resource classes are not equal, 
the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a34bbe15-f13f-4034-b2f1-fea3e58c579e">ResUtilResourcesEqual</a>
 

 

