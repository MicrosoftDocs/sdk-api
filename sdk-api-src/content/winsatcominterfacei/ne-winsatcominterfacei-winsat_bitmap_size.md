---
UID: NE:winsatcominterfacei.__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0004
title: WINSAT_BITMAP_SIZE (winsatcominterfacei.h)
description: Defines the size of the bitmap to use to represent the WinSAT score.
helpviewer_keywords: ["WINSAT_BITMAP_SIZE","WINSAT_BITMAP_SIZE enumeration [WinSAT]","WINSAT_BITMAP_SIZE_NORMAL","WINSAT_BITMAP_SIZE_SMALL","winsat.winsat_bitmap_size","winsatcominterfacei/WINSAT_BITMAP_SIZE","winsatcominterfacei/WINSAT_BITMAP_SIZE_NORMAL","winsatcominterfacei/WINSAT_BITMAP_SIZE_SMALL"]
old-location: winsat\winsat_bitmap_size.htm
tech.root: WinSAT
ms.assetid: 5cc91824-f3d4-4c33-85df-b98c8d6ac0a1
ms.date: 12/05/2018
ms.keywords: WINSAT_BITMAP_SIZE, WINSAT_BITMAP_SIZE enumeration [WinSAT], WINSAT_BITMAP_SIZE_NORMAL, WINSAT_BITMAP_SIZE_SMALL, winsat.winsat_bitmap_size, winsatcominterfacei/WINSAT_BITMAP_SIZE, winsatcominterfacei/WINSAT_BITMAP_SIZE_NORMAL, winsatcominterfacei/WINSAT_BITMAP_SIZE_SMALL
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: WINSAT_BITMAP_SIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0004
 - winsatcominterfacei/__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0004
 - WINSAT_BITMAP_SIZE
 - winsatcominterfacei/WINSAT_BITMAP_SIZE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsatcominterfacei.h
api_name:
 - WINSAT_BITMAP_SIZE
---

# WINSAT_BITMAP_SIZE enumeration


## -description

<p class="CCE_Message">[WINSAT_BITMAP_SIZE may be altered or unavailable for releases after Windows 8.1.]

Defines the size of the bitmap to use to represent the WinSAT score.

## -enum-fields

### -field WINSAT_BITMAP_SIZE_SMALL:0

Use a 32 x 24 bitmap (size is in pixels).

### -field WINSAT_BITMAP_SIZE_NORMAL:1

Use an 80 x 80 bitmap (size is in pixels).

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap">IProvideWinSATVisuals::get_Bitmap</a>
