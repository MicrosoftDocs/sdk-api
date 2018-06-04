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

# _MF_ATTRIBUTES_MATCH_TYPE enumeration


## -description



Specifies how to compare the attributes on two objects.




## -enum-fields




### -field MF_ATTRIBUTES_MATCH_OUR_ITEMS

Check whether all the attributes in <i>pThis</i> exist in <i>pTheirs</i> and have the same data, where <i>pThis</i> is the object whose <a href="https://msdn.microsoft.com/library/windows/hardware/hh406436">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.


### -field MF_ATTRIBUTES_MATCH_THEIR_ITEMS

Check whether all the attributes in <i>pTheirs</i> exist in <i>pThis</i> and have the same data, where <i>pThis</i> is the object whose <a href="https://msdn.microsoft.com/library/windows/hardware/hh406436">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.


### -field MF_ATTRIBUTES_MATCH_ALL_ITEMS

Check whether both objects have identical attributes with the same data.


### -field MF_ATTRIBUTES_MATCH_INTERSECTION

Check whether the attributes that exist in both objects have the same data.


### -field MF_ATTRIBUTES_MATCH_SMALLER

Find the object with the fewest number of attributes, and check if those attributes exist in the other object and have the same data.


## -see-also




<a href="https://msdn.microsoft.com/1d0c9d1c-448d-4851-b183-94b04acb2ab5">IMFAttributes::Compare</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

