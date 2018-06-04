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

# PDX_SETSTATE callback function


## -description


The<i> DxSetState</i> callback function is called when a client of the video miniport driver decides it wants to switch from bob mode to weave mode, and vice versa. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - SetStateInInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550319">DDSETSTATEININFO</a> structure that contains the surface and VPE object information.


#### - SetStateOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550320">DDSETSTATEOUTINFO</a> structure that contains the state information for the hardware video port.


## -returns



<i>DxSetState</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The surface data passed contains the new state. If the new state is not supported, the video miniport driver should fail the call. 

If the new state requires the device to revert from hardware autoflipping to software autoflipping, the video miniport driver should set members of the DDSETSTATEOUTINFO structure at <i>SetStateOutInfo</i> as follows:

<ul>
<li>
The <b>dwSoftwareAutoflip</b> member equal to 1.

</li>
<li>
The <b>dwSurfaceIndex</b> member equal to the current position in the auto-flip list of the surface receiving hardware video port data.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550319">DDSETSTATEININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550320">DDSETSTATEOUTINFO</a>
 

 

