---
UID: NS:ddkmapi._DDGETPOLARITYOUT
title: "_DDGETPOLARITYOUT"
author: windows-sdk-content
description: The DDGETPOLARITYOUT structure contains the requested polarity information.
old-location: display\ddgetpolarityout.htm
tech.root: display
ms.assetid: f659ceff-39ba-4d74-98f2-ad12be730ffb
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*LPDDGETPOLARITYOUT, DDGETPOLARITYOUT, DDGETPOLARITYOUT structure [Display Devices], LPDDGETPOLARITYOUT, LPDDGETPOLARITYOUT structure pointer [Display Devices], _DDGETPOLARITYOUT, ddkmapi/DDGETPOLARITYOUT, ddkmapi/LPDDGETPOLARITYOUT, ddstrcts_fa20dcb8-4818-4c9d-8378-93c0fda09eff.xml, display.ddgetpolarityout"
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
 - DDGETPOLARITYOUT
product: Windows
targetos: Windows
req.typenames: DDGETPOLARITYOUT, *LPDDGETPOLARITYOUT
req.redist: 
---

# _DDGETPOLARITYOUT structure


## -description


The DDGETPOLARITYOUT structure contains the requested polarity information. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/613fe2ac-010a-493c-87eb-aa7503673e9e">DD_DXAPI_GET_POLARITY</a> operations. A return code of DD_OK indicates success.


### -field bPolarity

Specifies whether the field is an even or odd field of an interlaced video signal. A value of <b>TRUE</b> indicates even, <b>FALSE</b> indicates odd. 


## -see-also




<a href="https://msdn.microsoft.com/613fe2ac-010a-493c-87eb-aa7503673e9e">DD_DXAPI_GET_POLARITY</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

