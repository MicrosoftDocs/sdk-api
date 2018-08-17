---
UID: NC:dxmini.PDX_LOCK
title: PDX_LOCK
author: windows-sdk-content
description: The DxLock callback function is called when a client of the video miniport driver wants access to the frame buffer.
old-location: display\dxlock.htm
old-project: display
ms.assetid: 1eeeb68b-9098-4030-924a-634e79c3e682
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DxLock, DxLock callback function [Display Devices], PDX_LOCK, PDX_LOCK callback, VideoMiniPort_DxApiFunctions_35d3fff6-f764-4dd7-a239-74dde81cdebb.xml, display.dxlock, dxmini/DxLock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dxmini.h
req.include-header: Dxmini.h
req.redist: 
req.target-type: Desktop
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
tech.root: 
req.typenames: DXGI_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxmini.h
api_name:
 - DxLock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

Points to a <a href="https://msdn.microsoft.com/4a4fb927-9037-4a42-9052-8b14ff899fe0">DDLOCKININFO</a> structure that contains the surface information for the lock.


#### - LockOutInfo

Points to a <a href="https://msdn.microsoft.com/a29ec594-c5f9-46e4-a8c2-95e24e2ddb2d">DDLOCKOUTINFO</a> structure that contains the surface in the frame buffer.


## -returns



<i>DxLock</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The <a href="https://msdn.microsoft.com/4a4fb927-9037-4a42-9052-8b14ff899fe0">DDLOCKININFO</a> and <a href="https://msdn.microsoft.com/a29ec594-c5f9-46e4-a8c2-95e24e2ddb2d">DDLOCKOUTINFO</a> structures contain surface information.




## -see-also




<a href="https://msdn.microsoft.com/4a4fb927-9037-4a42-9052-8b14ff899fe0">DDLOCKININFO</a>



<a href="https://msdn.microsoft.com/a29ec594-c5f9-46e4-a8c2-95e24e2ddb2d">DDLOCKOUTINFO</a>
 

 

