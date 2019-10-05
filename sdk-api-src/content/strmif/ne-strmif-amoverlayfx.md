---
UID: NE:strmif.AMOVERLAYFX
title: AMOVERLAYFX (strmif.h)
author: windows-sdk-content
description: Specifies effects on a DirectDraw hardware overlay surface.
old-location: dshow\amoverlayfx.htm
tech.root: DirectShow
ms.assetid: fa984504-5175-4b94-8a75-d294cd9546a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AMOVERFX_DEINTERLACE, AMOVERFX_MIRRORLEFTRIGHT, AMOVERFX_MIRRORUPDOWN, AMOVERFX_NOFX, AMOVERLAYFX, AMOVERLAYFX enumeration [DirectShow], AMOVERLAYFXEnumeration, dshow.amoverlayfx, strmif/AMOVERFX_DEINTERLACE, strmif/AMOVERFX_MIRRORLEFTRIGHT, strmif/AMOVERFX_MIRRORUPDOWN, strmif/AMOVERFX_NOFX, strmif/AMOVERLAYFX
ms.topic: enum
f1_keywords: 
 - "strmif/AMOVERLAYFX"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

When used in <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-queryoverlayfxcaps">IAMOverlayFX::QueryOverlayFXCaps</a>, this flag specifies whether the hardware can support the DirectDraw 7 DDOVERFX_DEINTERLACE hint. When used with the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-getoverlayfx">IAMOverlayFX::GetOverlayFX</a> or <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamoverlayfx-setoverlayfx">IAMOverlayFX::SetOverlayFX</a> methods, this flag indicates that the overlay should be deinterlaced if possible.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamoverlayfx">IAMOverlayFX Interface</a>
 

 

