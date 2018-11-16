---
UID: NS:ddrawint._DD_MOTIONCOMP_LOCAL
title: "_DD_MOTIONCOMP_LOCAL"
author: windows-sdk-content
description: The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object.
old-location: display\dd_motioncomp_local.htm
tech.root: display
ms.assetid: 41cde03a-f9da-4701-a0df-0dba0c17ba26
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PDD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL structure [Display Devices], _DD_MOTIONCOMP_LOCAL, ddrawint/DD_MOTIONCOMP_LOCAL, ddstrcts_cc4890b6-b2b6-484c-b979-4627fa902d7d.xml, display.dd_motioncomp_local"
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
 - DD_MOTIONCOMP_LOCAL
product: Windows
targetos: Windows
req.typenames: "*PDD_MOTIONCOMP_LOCAL, DD_MOTIONCOMP_LOCAL"
req.redist: 
---

# _DD_MOTIONCOMP_LOCAL structure


## -description


The DD_MOTIONCOMP_LOCAL structure contains local data for each individual Microsoft DirectDraw motion compensation object. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.


### -field guid

Specifies a GUID that describes the motion compensation process being used.


### -field dwUncompWidth

Indicates the width in pixels of the uncompressed output frame. 


### -field dwUncompHeight

Indicates the height in pixels of the uncompressed output frame. 


### -field ddUncompPixelFormat

Specifies a <a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame. 


### -field dwDriverReserved1


### -field dwDriverReserved2


### -field dwDriverReserved3

Are reserved for use by the display driver. 


### -field lpDriverReserved1


### -field lpDriverReserved2


### -field lpDriverReserved3

Are reserved for use by the display driver. 

