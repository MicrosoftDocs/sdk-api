---
UID: NS:ddkmapi._DDSETFIELDNUM
title: "_DDSETFIELDNUM"
author: windows-driver-content
description: The DDSETFIELDNUM structure contains the handles and the field number.
old-location: display\ddsetfieldnum.htm
old-project: display
ms.assetid: 442a4bbf-e3d9-4b06-99c4-1ffcf708a15c
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*LPDDSETFIELDNUM, DDSETFIELDNUM, DDSETFIELDNUM structure [Display Devices], LPDDSETFIELDNUM, LPDDSETFIELDNUM structure pointer [Display Devices], _DDSETFIELDNUM, ddkmapi/DDSETFIELDNUM, ddkmapi/LPDDSETFIELDNUM, ddstrcts_d8753497-b27b-4bd5-adcd-5b76e2169535.xml, display.ddsetfieldnum"
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
req.typenames: DDSETFIELDNUM, *LPDDSETFIELDNUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddkmapi.h
api_name:
-	DDSETFIELDNUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDSETFIELDNUM structure


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551507">DD_DXAPI_SET_VP_FIELD_NUMBER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

