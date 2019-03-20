---
UID: NS:ddkmapi._DDSETFIELDNUM
title: DDSETFIELDNUM (ddkmapi.h)
author: windows-sdk-content
description: The DDSETFIELDNUM structure contains the handles and the field number.
old-location: display\ddsetfieldnum.htm
tech.root: display
ms.assetid: 442a4bbf-e3d9-4b06-99c4-1ffcf708a15c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDSETFIELDNUM, DDSETFIELDNUM, DDSETFIELDNUM structure [Display Devices], LPDDSETFIELDNUM, LPDDSETFIELDNUM structure pointer [Display Devices], ddkmapi/DDSETFIELDNUM, ddkmapi/LPDDSETFIELDNUM, ddstrcts_d8753497-b27b-4bd5-adcd-5b76e2169535.xml, display.ddsetfieldnum"
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
 - DDSETFIELDNUM
product: Windows
targetos: Windows
req.typenames: DDSETFIELDNUM, *LPDDSETFIELDNUM
req.redist: 
---

# DDSETFIELDNUM structure


## -description


The DDSETFIELDNUM structure contains the handles and the field number.


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.


### -field hVideoPort

Specifies the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object handle.


### -field dwFieldNum

Specifies the hardware video port's field number to be set.


## -see-also




<a href="https://msdn.microsoft.com/316efd72-2bb7-4aa1-9a65-82d6bb558956">DD_DXAPI_SET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

