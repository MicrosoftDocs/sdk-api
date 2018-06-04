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

# tagINTERVAL_LIMIT_KIND enumeration


## -description


These values are returned by <a href="https://msdn.microsoft.com/631f3ec2-cf8f-4c20-8933-c83bac4b3d58">IInterval::GetLimits</a> as pairs to specify a range with an upper and lower limit. <b>INTERVAL_LIMIT_KIND</b> identifies whether the ranges include or exclude the upper and lower values of the range, and whether a range begins or ends in infinity.


## -enum-fields




### -field ILK_EXPLICIT_INCLUDED

The value is included in the range. For example, an integer range of numbers that is equal to or greater than 3 and less than or equal to 6 includes both 3 and 6. So the values 3 and 6 would both be returned with <b>ILK_EXPLICIT_INCLUDED</b>.


### -field ILK_EXPLICIT_EXCLUDED

The value bounds the range but is not included in the range. For example, an integer range that is greater than 3 but less than 6 excludes both 3 and 6. So the values would both be returned with <b>ILK_EXPLICIT_EXCLUDED</b>.


### -field ILK_NEGATIVE_INFINITY

This is typically used as a lower bound. The specified value is ignored because the range begins (or ends) at negative infinity. For example, an integer range that includes every value less than 6 would have <b>ILK_NEGATIVE_INFINITY</b> for the lower bound and 6 and <b>ILK_EXPLICIT_EXCLUDED</b> for the upper bound. 




### -field ILK_POSITIVE_INFINITY

This is typically used as an upper bound. The specified value is ignored because the range begins (or ends) at positive infinity. For example, an integer range that includes every value greater than or equal to 3 would have <b>ILK_EXPLICIT_INCLUDED</b> and 3 for the lower bound and <b>ILK_POSITIVE_INFINITY</b> for the upper bound. 



