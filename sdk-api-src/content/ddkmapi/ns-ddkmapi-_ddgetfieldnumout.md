---
UID: NS:ddkmapi._DDGETFIELDNUMOUT
title: "_DDGETFIELDNUMOUT"
author: windows-sdk-content
description: The DDGETFIELDNUMOUT structure contains the hardware video port's field number.
old-location: display\ddgetfieldnumout.htm
tech.root: display
ms.assetid: 6af9d0be-03b7-4153-a4d6-cf36afe4fd0e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPDDGETFIELDNUMOUT, DDGETFIELDNUMOUT, DDGETFIELDNUMOUT structure [Display Devices], LPDDGETFIELDNUMOUT, LPDDGETFIELDNUMOUT structure pointer [Display Devices], _DDGETFIELDNUMOUT, ddkmapi/DDGETFIELDNUMOUT, ddkmapi/LPDDGETFIELDNUMOUT, ddstrcts_a52a121b-2050-41c3-a5ee-6ad474e3a666.xml, display.ddgetfieldnumout"
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
 - DDGETFIELDNUMOUT
product: Windows
targetos: Windows
req.typenames: DDGETFIELDNUMOUT, *LPDDGETFIELDNUMOUT
req.redist: 
---

# _DDGETFIELDNUMOUT structure


## -description


The DDGETFIELDNUMOUT structure contains the hardware video port's field number. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/6d6464f3-cece-405e-af0c-b2a54fa2fc20">DD_DXAPI_GET_VP_FIELD_NUMBER</a> operations. A return code of DD_OK indicates success.


### -field dwFieldNum

Specifies the hardware video port's field number.


## -see-also




<a href="https://msdn.microsoft.com/6d6464f3-cece-405e-af0c-b2a54fa2fc20">DD_DXAPI_GET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

