---
UID: NS:ddkmapi._DDCAPBUFFINFO
title: DDCAPBUFFINFO
author: windows-sdk-content
description: The DDCAPBUFFINFO structure contains the capture information.
old-location: display\ddcapbuffinfo.htm
tech.root: display
ms.assetid: 8286c433-2183-4751-be8a-30cb9cd9146d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDCAPBUFFINFO, DDCAPBUFFINFO, DDCAPBUFFINFO structure [Display Devices], LPDDCAPBUFFINFO, LPDDCAPBUFFINFO structure pointer [Display Devices], ddkmapi/DDCAPBUFFINFO, ddkmapi/LPDDCAPBUFFINFO, ddstrcts_c1b7049e-f505-419f-ba3e-53625521dae2.xml, display.ddcapbuffinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DDCAPBUFFINFO
product: Windows
targetos: Windows
req.typenames: DDCAPBUFFINFO, *LPDDCAPBUFFINFO
req.redist: 
---

# DDCAPBUFFINFO structure


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

Specifies the location in which DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for the <a href="https://msdn.microsoft.com/d7e6fd1c-8865-4f55-868c-856b2f875053">DD_DXAPI_ADDVPCAPTUREBUFFER</a> operation. Contains DD_OK if the capture buffer contains valid data.


## -see-also




<a href="https://msdn.microsoft.com/7ee3f5ce-987a-42c9-8681-5bcb9028178a">DDADDVPCAPTUREBUFF</a>



<a href="https://msdn.microsoft.com/d7e6fd1c-8865-4f55-868c-856b2f875053">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

