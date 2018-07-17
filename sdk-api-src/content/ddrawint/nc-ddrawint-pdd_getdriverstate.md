---
UID: NC:ddrawint.PDD_GETDRIVERSTATE
title: PDD_GETDRIVERSTATE
author: windows-sdk-content
description: The D3dGetDriverState function is used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.
old-location: display\d3dgetdriverstate.htm
old-project: display
ms.assetid: 6e1b0bce-1ac5-46e7-ae25-b0d3ce8580a0
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: D3dGetDriverState, D3dGetDriverState callback function [Display Devices], PDD_GETDRIVERSTATE, PDD_GETDRIVERSTATE callback, d3dfncs_e2c93c0f-5d2e-47b2-b8df-b527db9b121e.xml, ddrawint/D3dGetDriverState, display.d3dgetdriverstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - D3dGetDriverState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_GETDRIVERSTATE callback function


## -description


The <i>D3dGetDriverState</i> function is used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.


## -parameters




### -param Arg1








#### - pgdsd

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551551">DD_GETDRIVERSTATEDATA</a> structure that describes the state of the driver.


## -returns



<i>D3dGetDriverState</i> returns one of the following callback codes: 




## -remarks



All Direct3D drivers must support <i>D3dGetDriverState</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551551">DD_GETDRIVERSTATEDATA</a>
 

 

