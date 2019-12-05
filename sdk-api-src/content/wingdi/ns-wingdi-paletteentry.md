---
UID: NS:wingdi.tagPALETTEENTRY
title: PALETTEENTRY (wingdi.h)
description: Specifies the color and usage of an entry in a logical palette.
old-location: direct3d9\paletteentry.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\paletteentry.htm
ms.date: 12/05/2018
ms.keywords: '*LPPALETTEENTRY, *PPALETTEENTRY, 523c466d-5003-02e3-c336-f0e36539855e, LPPALETTEENTRY, LPPALETTEENTRY structure pointer [Direct3D 9], PALETTEENTRY, PALETTEENTRY structure [Direct3D 9], direct3d9.paletteentry, wingdi/LPPALETTEENTRY, wingdi/PALETTEENTRY'
ms.topic: struct
f1_keywords:
- wingdi/PALETTEENTRY
dev_langs:
- c++
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
targetos: Windows
req.typenames: PALETTEENTRY, *PPALETTEENTRY, *LPPALETTEENTRY
req.redist: 
ms.custom: 19H1
---

# PALETTEENTRY structure


## -description


Specifies the color and usage of an entry in a logical palette.


## -struct-fields




### -field peRed

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The red intensity value for the palette entry.


### -field peGreen

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The green intensity value for the palette entry.


### -field peBlue

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The blue intensity value for the palette entry.


### -field peFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The alpha intensity value for the palette entry. Note that as of DirectX 8, this member is treated differently than documented for Windows. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-structures">Direct3D Structures</a>
 

 

