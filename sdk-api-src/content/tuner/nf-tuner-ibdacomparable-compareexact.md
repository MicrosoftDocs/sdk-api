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

# IBDAComparable::CompareExact


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>CompareExact</b> method compares two objects to determine whether they contain the same tuning information.


## -parameters




### -param CompareTo [in]

Pointer to the <b>IDispatch</b> interface of the object that is to be compared with the object that implements the <b>IBDAComparable</b> interface.


### -param Result [out]

Pointer to a variable that receives the result of the comparison. If the result is 0, the two objects are the same. If the result is nonzero, the two objects are not the same.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method compares two objects to determine whether they contain the same tuning properties. The first object in the comparison is the object that implements the <b>IBDAComparable</b> interface that the method is called on. The <i>CompareTo</i> parameter specifies the second object.

This method compares all of the tuning properties of the two objects and their associated objects. In contrast, the <a href="https://msdn.microsoft.com/132c326e-053c-41be-b0fd-bea484fb0acd">CompareEquivalent</a> method compares only a subset of these properties.

For example, DirectShow implements the <b>IBDAComparable::CompareExact</b> method for a tune-request object to include both the tuning space and locator in the comparison. Thus, two DVB tuning requests are the same only if they both tune to the same DVB URL (with the same original network ID, transport stream ID, and service ID) <i>and</i> have the same modulation type.




## -see-also




<a href="https://msdn.microsoft.com/6f582ae2-d8c6-4d85-a01f-e98c6ee16021">IBDAComparable Interface</a>
 

 

