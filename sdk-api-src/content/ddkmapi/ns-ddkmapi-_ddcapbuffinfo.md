---
UID: NS:ddkmapi._DDCAPBUFFINFO
title: "_DDCAPBUFFINFO"
author: windows-sdk-content
description: The DDCAPBUFFINFO structure contains the capture information.
old-location: display\ddcapbuffinfo.htm
old-project: display
ms.assetid: 8286c433-2183-4751-be8a-30cb9cd9146d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPDDCAPBUFFINFO, DDCAPBUFFINFO, DDCAPBUFFINFO structure [Display Devices], LPDDCAPBUFFINFO, LPDDCAPBUFFINFO structure pointer [Display Devices], _DDCAPBUFFINFO, ddkmapi/DDCAPBUFFINFO, ddkmapi/LPDDCAPBUFFINFO, ddstrcts_c1b7049e-f505-419f-ba3e-53625521dae2.xml, display.ddcapbuffinfo"
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
req.typenames: DDCAPBUFFINFO, *LPDDCAPBUFFINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddkmapi.h
api_name:
-	DDCAPBUFFINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDCAPBUFFINFO structure


## -description


The DDCAPBUFFINFO structure contains the capture information. 


## -struct-fields




### -field dwFieldNumber

Indicates the internal field number of the field captured.


### -field bPolarity

Specifies whether the captured field is an even or odd field. A value of 0x00000001 indicates even, 0x00000000 indicates odd.


### -field liTimeStamp

Used by Microsoft DirectDraw and should be ignored by the driver.


### -field ddRVal

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a> operation. Contains DD_OK if the capture buffer contains valid data.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549199">DDADDVPCAPTUREBUFF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550599">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

