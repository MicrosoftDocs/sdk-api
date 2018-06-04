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

# AdjustableArrowCap class


## -description


The <b>AdjustableArrowCap</b> class is a subclass of the <a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>. This class builds a line cap that looks like an arrow.


## -remarks



A line cap is the shape on the end of a line. Use the 
				<a href="https://msdn.microsoft.com/23384bd0-94da-4c2a-9228-47cc0f0d18a7">Pen::SetCustomStartCap</a> and 
				<a href="https://msdn.microsoft.com/d7be905c-92fe-4a7e-9422-f60912461dc9">Pen::SetCustomEndCap</a> methods to associate an <b>AdjustableArrowCap</b> object with a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>
 object.



