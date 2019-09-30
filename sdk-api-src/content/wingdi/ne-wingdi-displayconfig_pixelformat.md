---
UID: NE:wingdi.__unnamed_enum_5
title: DISPLAYCONFIG_PIXELFORMAT (wingdi.h)
author: windows-sdk-content
description: The DISPLAYCONFIG_PIXELFORMAT enumeration specifies pixel format in various bits per pixel (BPP) values.
old-location: display\displayconfig_pixelformat.htm
tech.root: display
ms.assetid: dca8433d-89a9-492c-bebb-6a28f485896c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_d2979717-6f47-4872-9be2-8b19b06ce2f2.xml, DISPLAYCONFIG_PIXELFORMAT, DISPLAYCONFIG_PIXELFORMAT enumeration [Display Devices], DISPLAYCONFIG_PIXELFORMAT_16BPP, DISPLAYCONFIG_PIXELFORMAT_24BPP, DISPLAYCONFIG_PIXELFORMAT_32BPP, DISPLAYCONFIG_PIXELFORMAT_8BPP, DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32, DISPLAYCONFIG_PIXELFORMAT_NONGDI, display.displayconfig_pixelformat, wingdi/DISPLAYCONFIG_PIXELFORMAT, wingdi/DISPLAYCONFIG_PIXELFORMAT_16BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_24BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_32BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_8BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32, wingdi/DISPLAYCONFIG_PIXELFORMAT_NONGDI
ms.topic: enum
f1_keywords: 
 - "wingdi/DISPLAYCONFIG_PIXELFORMAT"
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
 - wingdi.h
api_name:
 - DISPLAYCONFIG_PIXELFORMAT
targetos: Windows
req.typenames: DISPLAYCONFIG_PIXELFORMAT
req.redist: 
ms.custom: 19H1
---

# DISPLAYCONFIG_PIXELFORMAT enumeration


## -description


The DISPLAYCONFIG_PIXELFORMAT enumeration specifies pixel format in various bits per pixel (BPP) values.


## -enum-fields




### -field DISPLAYCONFIG_PIXELFORMAT_8BPP

Indicates 8 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_16BPP

Indicates 16 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_24BPP

Indicates 24 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_32BPP

Indicates 32 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_NONGDI

Indicates that the current display is not an 8, 16, 24, or 32 BPP GDI desktop mode. For example, a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> function returns DISPLAYCONFIG_PIXELFORMAT_NONGDI if a DirectX application previously set the desktop to A2R10G10B10 format. A call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> function fails if any pixel formats for active paths are set to DISPLAYCONFIG_PIXELFORMAT_NONGDI. 


### -field DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
 

 

