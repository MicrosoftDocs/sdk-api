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

# LinearGradientBrush::GetBlendCount


## -description


The <b>LinearGradientBrush::GetBlendCount</b> method gets the number of blend factors currently set for this 
			<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of blend factors currently set for this 
						<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object. If no custom blend has been set by using <a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a>, or if invalid positions were passed to <b>LinearGradientBrush::SetBlend</b>, then <a href="https://msdn.microsoft.com/2eadd02c-75fd-4317-a925-68a5d32b139e">LinearGradientBrush::GetBlend</a> returns 1.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2eadd02c-75fd-4317-a925-68a5d32b139e">LinearGradientBrush::GetBlend</a>



<a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>
 

 

