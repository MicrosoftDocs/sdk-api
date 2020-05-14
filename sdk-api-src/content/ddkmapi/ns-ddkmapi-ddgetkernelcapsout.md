---
UID: NS:ddkmapi._DDGETKERNELCAPSOUT
title: DDGETKERNELCAPSOUT (ddkmapi.h)
description: The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object.helpviewer_keywords: ["*LPDDGETKERNELCAPSOUT","DDGETKERNELCAPSOUT","DDGETKERNELCAPSOUT structure [Display Devices]","LPDDGETKERNELCAPSOUT","LPDDGETKERNELCAPSOUT structure pointer [Display Devices]","ddkmapi/DDGETKERNELCAPSOUT","ddkmapi/LPDDGETKERNELCAPSOUT","ddstrcts_4879ba8e-459c-4b10-b43a-854a85d4e10f.xml","display.ddgetkernelcapsout"]
old-location: display\ddgetkernelcapsout.htm
tech.root: display
ms.assetid: 7c0ccd18-3892-4512-9957-1ac01fa83f0f
ms.date: 12/05/2018
ms.keywords: '*LPDDGETKERNELCAPSOUT, DDGETKERNELCAPSOUT, DDGETKERNELCAPSOUT structure [Display Devices], LPDDGETKERNELCAPSOUT, LPDDGETKERNELCAPSOUT structure pointer [Display Devices], ddkmapi/DDGETKERNELCAPSOUT, ddkmapi/LPDDGETKERNELCAPSOUT, ddstrcts_4879ba8e-459c-4b10-b43a-854a85d4e10f.xml, display.ddgetkernelcapsout'
f1_keywords:
- ddkmapi/DDGETKERNELCAPSOUT
dev_langs:
- c++
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
targetos: Windows
req.typenames: DDGETKERNELCAPSOUT, *LPDDGETKERNELCAPSOUT
req.redist: 
ms.custom: 19H1
---

# DDGETKERNELCAPSOUT structure


## -description


The DDGETKERNELCAPSOUT structure contains the capabilities of the Microsoft DirectDraw object. 


## -struct-fields




### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a> function for <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550629(v=vs.85)">DD_DXAPI_GETKERNELCAPS</a> operations. A return code of DD_OK indicates success.


### -field dwCaps

Can be any combination of the capabilities in the <b>dwCaps</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ddkernel/ns-ddkernel-ddkernelcaps">DDKERNELCAPS</a> structure.


### -field dwIRQCaps

Can be a combination of the flags in the <b>dwIRQCaps</b> member of DDKERNELCAPS.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550629(v=vs.85)">DD_DXAPI_GETKERNELCAPS</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/dxapi/nf-dxapi-dxapi">DxApi</a>
 

 

