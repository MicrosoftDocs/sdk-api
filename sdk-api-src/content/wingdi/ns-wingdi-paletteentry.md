---
UID: NS:wingdi.tagPALETTEENTRY
title: PALETTEENTRY (wingdi.h)
author: windows-sdk-content
description: Specifies the color and usage of an entry in a logical palette.
old-location: direct3d9\paletteentry.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\paletteentry.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPALETTEENTRY, *PPALETTEENTRY, 523c466d-5003-02e3-c336-f0e36539855e, LPPALETTEENTRY, LPPALETTEENTRY structure pointer [Direct3D 9], PALETTEENTRY, PALETTEENTRY structure [Direct3D 9], direct3d9.paletteentry, wingdi/LPPALETTEENTRY, wingdi/PALETTEENTRY"
ms.topic: struct
req.header: wingdi.h
req.include-header: 
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
 - Wingdi.h
api_name:
 - PALETTEENTRY
product: Windows
targetos: Windows
req.typenames: PALETTEENTRY, *PPALETTEENTRY, *LPPALETTEENTRY
req.redist: 
---

# PALETTEENTRY structure


## -description


Specifies the color and usage of an entry in a logical palette.


## -struct-fields




### -field peRed

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The red intensity value for the palette entry.


### -field peGreen

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The green intensity value for the palette entry.


### -field peBlue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The blue intensity value for the palette entry.


### -field peFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The alpha intensity value for the palette entry. Note that as of DirectX 8, this member is treated differently than documented for Windows. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

