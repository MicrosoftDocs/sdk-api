---
UID: NS:ddkmapi._DDGETKERNELCAPSOUT
title: "_DDGETKERNELCAPSOUT"
author: windows-sdk-content
description: The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object.
old-location: display\ddgetkernelcapsout.htm
old-project: display
ms.assetid: 7c0ccd18-3892-4512-9957-1ac01fa83f0f
ms.author: windowssdkdev
ms.date: 05/10/2018
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
req.typenames: DDGETKERNELCAPSOUT, *LPDDGETKERNELCAPSOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddkmapi.h
api_name:
-	DDGETKERNELCAPSOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDGETKERNELCAPSOUT structure


## -description


The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for <a href="https://msdn.microsoft.com/library/windows/hardware/ff550629">DD_DXAPI_GETKERNELCAPS</a> operations. A return code of DD_OK indicates success.


### -field dwCaps

Can be any combination of the capabilities in the <b>dwCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549593">DDKERNELCAPS</a> structure.


### -field dwIRQCaps

Can be a combination of the flags in the <b>dwIRQCaps</b> member of DDKERNELCAPS.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550629">DD_DXAPI_GETKERNELCAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

