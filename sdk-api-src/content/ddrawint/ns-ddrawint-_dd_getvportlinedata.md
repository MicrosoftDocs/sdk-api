---
UID: NS:ddrawint._DD_GETVPORTLINEDATA
title: "_DD_GETVPORTLINEDATA"
author: windows-driver-content
description: The DD_GETVPORTLINEDATA structure contains the current line number of the hardware video port.
old-location: display\dd_getvportlinedata.htm
old-project: display
ms.assetid: d8b2803c-38be-40ea-b46b-4bab1ce55534
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PDD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA structure [Display Devices], _DD_GETVPORTLINEDATA, ddrawint/DD_GETVPORTLINEDATA, ddstrcts_81a8dc13-0681-4135-a74a-f7aa22408156.xml, display.dd_getvportlinedata"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: "*PDD_GETVPORTLINEDATA, DD_GETVPORTLINEDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_GETVPORTLINEDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_GETVPORTLINEDATA structure


## -description


The DD_GETVPORTLINEDATA structure contains the current line number of the hardware video port.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object.


### -field dwLine

Specifies the location in which the driver should write the current line number on the hardware video port.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/6c0cfa87-bc16-47a6-8106-e5a1b1456813">DdVideoPortGetLine</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetVideoPortLine

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/6c0cfa87-bc16-47a6-8106-e5a1b1456813">DdVideoPortGetLine</a>
 

 

