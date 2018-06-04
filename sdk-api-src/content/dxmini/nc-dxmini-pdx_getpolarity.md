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

# PDX_GETPOLARITY callback function


## -description


The<i> DxGetPolarity</i> callback function returns the polarity (even or odd) of the current field being written by the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - GetPolarityInInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549461">DDGETPOLARITYININFO</a> structure that contains the VPE object from which to get the polarity information.


#### - GetPolarityOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549481">DDGETPOLARITYOUTINFO</a> structure that contains the polarity information for the specified VPE object.


#### - HwDeviceExtension

Points to the miniport driver's device extension.


## -returns



<i>DxGetPolarity</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff549461">DDGETPOLARITYININFO</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff549481">DDGETPOLARITYOUTINFO</a> structures contain VPE object information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549461">DDGETPOLARITYININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549481">DDGETPOLARITYOUTINFO</a>
 

 

