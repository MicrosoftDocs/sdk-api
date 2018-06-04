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

# PATHOBJ_vEnumStart function


## -description


The <b>PATHOBJ_vEnumStart</b> function notifies a given PATHOBJ structure that the driver will be calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a> to enumerate lines and/or curves in the path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure whose lines and/or curves are to be enumerated.


## -returns



None




## -remarks



<b>PATHOBJ_vEnumStart</b> can be called at any time to restart an enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568851">PATHOBJ_bEnum</a>
 

 

