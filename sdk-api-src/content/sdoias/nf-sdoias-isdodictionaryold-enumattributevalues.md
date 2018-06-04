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

# ISdoDictionaryOld::EnumAttributeValues


## -description


The 
<b>EnumAttributeValues</b> method retrieves the values for an enumerable attribute.


## -parameters




### -param Id [in]

Specifies the ID of the attribute.


### -param pValueIds [out]

On successful return points to a 
<a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of value IDs for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VT_EMPTY</a> variant.


### -param pValuesDesc [out]

On successful return points to a 
<a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of value descriptions for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VT_EMPTY</a> variant.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The return value is S_OK even if the attribute is not enumerable.




## -see-also




<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

