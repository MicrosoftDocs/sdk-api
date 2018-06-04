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

# ID3DUserDefinedAnnotation::EndEvent


## -description


Marks the end of a section of event code.


## -parameters






## -returns



Returns the number of previous calls to the <a href="https://msdn.microsoft.com/38FC7BFA-A01E-4537-88F1-836AE03C9A07">ID3DUserDefinedAnnotation::BeginEvent</a> method that have not yet been finalized by calls to <b>EndEvent</b>.

The return value is –1 if the calling application is not running under a Direct3D profiling tool.




## -remarks



You call the <a href="https://msdn.microsoft.com/38FC7BFA-A01E-4537-88F1-836AE03C9A07">BeginEvent</a> method to mark the beginning of the section of event code.

A user can visualize the event when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>EndEvent</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.




## -see-also




<a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a>
 

 

