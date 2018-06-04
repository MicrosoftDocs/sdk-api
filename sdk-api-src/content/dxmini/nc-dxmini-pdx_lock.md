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

# PDX_LOCK callback function


## -description


The<i> DxLock</i> callback function is called when a client of the video miniport driver wants access to the frame buffer. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - LockInInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549615">DDLOCKININFO</a> structure that contains the surface information for the lock.


#### - LockOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549635">DDLOCKOUTINFO</a> structure that contains the surface in the frame buffer.


## -returns



<i>DxLock</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff549615">DDLOCKININFO</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff549635">DDLOCKOUTINFO</a> structures contain surface information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549615">DDLOCKININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549635">DDLOCKOUTINFO</a>
 

 

