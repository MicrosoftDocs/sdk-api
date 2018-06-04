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

# PDD_SURFCB_GETFLIPSTATUS callback function


## -description


The <b>DdGetFlipStatus</b> callback function determines whether the most recently requested flip on a surface has occurred.


## -parameters




### -param Arg1








#### - lpGetFlipStatus

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551564">DD_GETFLIPSTATUSDATA</a> structure that contains the information required to perform the flip status query.


## -returns



<b>DdGetFlipStatus</b> returns one of the following callback codes:




## -remarks



The driver should report its flip status based on the flag set in the <b>dwFlags</b> member of the structure that <b>lpGetFlipStatus</b> points to as follows:

<ul>
<li>
If the flag is DDGFS_CANFLIP, the driver should determine whether the surface is currently involved in a flip. If a flip or a blit is not in progress and if the hardware is otherwise capable of currently accepting a flip request, the driver should return DD_OK in <b>ddRVal</b>. If a flip is in progress or if the hardware cannot currently accept a flip request, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING.

</li>
<li>
If the flag is DDGFS_ISFLIPDONE, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING if a flip is currently in progress; otherwise it should return DD_OK.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551564">DD_GETFLIPSTATUSDATA</a>
 

 

