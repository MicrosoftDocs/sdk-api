---
UID: NE:strmif.AMOVERLAYFX
title: AMOVERLAYFX
author: windows-sdk-content
description: Specifies effects on a DirectDraw hardware overlay surface.
old-location: dshow\amoverlayfx.htm
tech.root: DirectShow
ms.assetid: fa984504-5175-4b94-8a75-d294cd9546a4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AMOVERFX_DEINTERLACE, AMOVERFX_MIRRORLEFTRIGHT, AMOVERFX_MIRRORUPDOWN, AMOVERFX_NOFX, AMOVERLAYFX, AMOVERLAYFX enumeration [DirectShow], AMOVERLAYFXEnumeration, dshow.amoverlayfx, strmif/AMOVERFX_DEINTERLACE, strmif/AMOVERFX_MIRRORLEFTRIGHT, strmif/AMOVERFX_MIRRORUPDOWN, strmif/AMOVERFX_NOFX, strmif/AMOVERLAYFX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
 - strmif.h
api_name:
 - AMOVERLAYFX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AMOVERLAYFX enumeration


## -description



Specifies effects on a DirectDraw hardware overlay surface.




## -enum-fields




### -field AMOVERFX_NOFX

Normal video (no effects).
          


### -field AMOVERFX_MIRRORLEFTRIGHT

Mirror the overlay across the vertical axis.
          


### -field AMOVERFX_MIRRORUPDOWN

Mirror the overlay across the horizontal axis.
          


### -field AMOVERFX_DEINTERLACE

When used in <a href="https://msdn.microsoft.com/01fdbe3d-bec7-4e66-87c5-b7e6c1044e8a">IAMOverlayFX::QueryOverlayFXCaps</a>, this flag specifies whether the hardware can support the DirectDraw 7 DDOVERFX_DEINTERLACE hint. When used with the <a href="https://msdn.microsoft.com/f8232fcf-a0d8-4155-941e-8613c09b4bbf">IAMOverlayFX::GetOverlayFX</a> or <a href="https://msdn.microsoft.com/08e44f4e-924a-4a4d-9fc5-c13b3c21c038">IAMOverlayFX::SetOverlayFX</a> methods, this flag indicates that the overlay should be deinterlaced if possible.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/6bc78464-8c9e-4016-b9aa-6589d53d45bf">IAMOverlayFX Interface</a>
 

 

