---
UID: NF:directmanipulation.IDirectManipulationFrameInfoProvider.GetNextFrameInfo
title: IDirectManipulationFrameInfoProvider::GetNextFrameInfo
author: windows-sdk-content
description: Retrieves the composition timing information from the compositor.
old-location: directmanipulation\idirectmanipulationframeinfoprovider_getnextframeinfo.htm
tech.root: directmanipulation
ms.assetid: 3f561b81-241f-4f7a-bb5f-a89faf253c98
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNextFrameInfo, GetNextFrameInfo method [Direct Manipulation], GetNextFrameInfo method [Direct Manipulation],IDirectManipulationFrameInfoProvider interface, IDirectManipulationFrameInfoProvider interface [Direct Manipulation],GetNextFrameInfo method, IDirectManipulationFrameInfoProvider.GetNextFrameInfo, IDirectManipulationFrameInfoProvider::GetNextFrameInfo, directmanipulation.idirectmanipulationframeinfoprovider_getnextframeinfo, directmanipulation/IDirectManipulationFrameInfoProvider::GetNextFrameInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationFrameInfoProvider.GetNextFrameInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationFrameInfoProvider::GetNextFrameInfo


## -description


Retrieves the composition timing information from the compositor.


## -parameters




### -param time [out]

The current time, in milliseconds.


### -param processTime [out]

The time, in milliseconds, when the compositor begins constructing the next frame.


### -param compositionTime [out]

The time, in milliseconds, when the compositor finishes composing and drawing the next frame on the screen.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The system implementation of <a href="https://msdn.microsoft.com/15B7CA2A-DEC3-479B-BD41-38A57037002F">IDirectManipulationFrameInfoProvider</a> uses <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a>. <a href="https://msdn.microsoft.com/C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A">GetFrameStatistics</a> is used to calculate the parameter values for <b>GetNextFrameInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>



<a href="https://msdn.microsoft.com/15B7CA2A-DEC3-479B-BD41-38A57037002F">IDirectManipulationFrameInfoProvider</a>
 

 

