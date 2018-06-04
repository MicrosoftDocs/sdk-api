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

# Point::Equals


## -description


The <b>Point::Equals</b> method determines whether two 
			<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.


## -parameters




### -param point [in]

Type: <b>const Point&amp;</b>

Reference to a 
					<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> object that is compared to this 
					<b>Point</b> object. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> objects are equal, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>



<a href="https://msdn.microsoft.com/751eea61-b0c6-4112-bf0b-2936d12fb97e">Point::operator+</a>



<a href="https://msdn.microsoft.com/bcd6e8db-7584-4209-8c0a-6ce64c8724ce">Point::operator-</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 

