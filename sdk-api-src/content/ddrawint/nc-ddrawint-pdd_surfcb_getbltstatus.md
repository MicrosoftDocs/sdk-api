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

# PDD_SURFCB_GETBLTSTATUS callback function


## -description


The <b>DdGetBltStatus</b> callback function queries the blit status of the specified surface.


## -parameters




### -param Arg1








#### - lpGetBltStatus

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551534">DD_GETBLTSTATUSDATA</a> structure that contains the information required to perform the blit status query.


## -returns



<b>DdGetBltStatus</b> returns one of the following callback codes:




## -remarks



The blit status that the driver returns is based on the <b>dwFlags</b> member of the structure that <i>lpGetBltStatus</i> points to, as follows:

<ul>
<li>
If the flag is DDGBS_CANBLT, the driver should determine whether the surface is currently involved in a flip. If a flip is not in progress and if the hardware is otherwise capable of currently accepting a blit request, the driver should return DD_OK in the <b>ddRVal</b> member of the structure that <i>lpGetBltStatus</i> points to. If a flip is in progress or if the hardware cannot currently accept another blit request, the driver should set the <b>ddRVal</b> member to DDERR_WASSTILLDRAWING.

</li>
<li>
If the flag is DDGBS_ISBLTDONE, the driver should set <b>ddRVal</b> to DDERR_WASSTILLDRAWING if a blit is currently in progress; otherwise it should return DD_OK.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551534">DD_GETBLTSTATUSDATA</a>



<a href="https://msdn.microsoft.com/28e0c827-33f1-4b83-9f20-bbb66bc0e14a">DdBlt</a>
 

 

