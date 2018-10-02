---
UID: NS:ddkmapi._DDGETKERNELCAPSOUT
title: "_DDGETKERNELCAPSOUT"
author: windows-sdk-content
description: The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object.
old-location: display\ddgetkernelcapsout.htm
tech.root: Display
ms.assetid: 7c0ccd18-3892-4512-9957-1ac01fa83f0f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDDGETKERNELCAPSOUT, DDGETKERNELCAPSOUT, DDGETKERNELCAPSOUT structure [Display Devices], LPDDGETKERNELCAPSOUT, LPDDGETKERNELCAPSOUT structure pointer [Display Devices], _DDGETKERNELCAPSOUT, ddkmapi/DDGETKERNELCAPSOUT, ddkmapi/LPDDGETKERNELCAPSOUT, ddstrcts_4879ba8e-459c-4b10-b43a-854a85d4e10f.xml, display.ddgetkernelcapsout"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDGETKERNELCAPSOUT
product: Windows
targetos: Windows
req.typenames: DDGETKERNELCAPSOUT, *LPDDGETKERNELCAPSOUT
req.redist: 
---

# _DDGETKERNELCAPSOUT structure


## -description


The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/8cb0fd51-cca3-442d-8988-ef0ae6fcb1b7">DD_DXAPI_GETKERNELCAPS</a> operations. A return code of DD_OK indicates success.


### -field dwCaps

Can be any combination of the capabilities in the <b>dwCaps</b> member of the <a href="https://msdn.microsoft.com/d02d26f5-34cf-4a3c-b67c-0f9191bb854b">DDKERNELCAPS</a> structure.


### -field dwIRQCaps

Can be a combination of the flags in the <b>dwIRQCaps</b> member of DDKERNELCAPS.


## -see-also




<a href="https://msdn.microsoft.com/8cb0fd51-cca3-442d-8988-ef0ae6fcb1b7">DD_DXAPI_GETKERNELCAPS</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

