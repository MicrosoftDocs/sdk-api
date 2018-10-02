---
UID: NS:ddrawint._DD_GETVPORTFLIPSTATUSDATA
title: "_DD_GETVPORTFLIPSTATUSDATA"
author: windows-sdk-content
description: The DD_GETVPORTFLIPSTATUSDATA structure contains the flip status information for the specified surface.
old-location: display\dd_getvportflipstatusdata.htm
tech.root: Display
ms.assetid: 64be9019-a75f-42db-a636-b767f87c1858
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA structure [Display Devices], _DD_GETVPORTFLIPSTATUSDATA, ddrawint/DD_GETVPORTFLIPSTATUSDATA, ddstrcts_a1239418-1670-477d-b96e-d21dc2b9647b.xml, display.dd_getvportflipstatusdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
 - ddrawint.h
api_name:
 - DD_GETVPORTFLIPSTATUSDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA"
req.redist: 
---

# _DD_GETVPORTFLIPSTATUSDATA structure


## -description


The DD_GETVPORTFLIPSTATUSDATA structure contains the flip status information for the specified surface.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field fpSurface

Points to the surface for which the flip status information is required. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/67a7aa80-2201-4bb7-919b-dd9ca1228f06">DdVideoPortGetFlipStatus</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetVideoPortFlipStatus

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/67a7aa80-2201-4bb7-919b-dd9ca1228f06">DdVideoPortGetFlipStatus</a>
 

 

