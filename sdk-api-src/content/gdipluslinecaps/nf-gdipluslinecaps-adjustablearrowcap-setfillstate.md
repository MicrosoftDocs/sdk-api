---
UID: NF:gdipluslinecaps.AdjustableArrowCap.SetFillState
title: AdjustableArrowCap::SetFillState (gdipluslinecaps.h)
description: The AdjustableArrowCap::SetFillState method sets the fill state of the arrow cap. If the arrow cap is not filled, only the outline is drawn.
helpviewer_keywords: ["AdjustableArrowCap class [GDI+]","SetFillState method","AdjustableArrowCap.SetFillState","AdjustableArrowCap::SetFillState","SetFillState","SetFillState method [GDI+]","SetFillState method [GDI+]","AdjustableArrowCap class","_gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_","gdiplus._gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_"]
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcapclass\adjustablearrowcapmethods\setfillstate.htm
ms.date: 12/05/2018
ms.keywords: AdjustableArrowCap class [GDI+],SetFillState method, AdjustableArrowCap.SetFillState, AdjustableArrowCap::SetFillState, SetFillState, SetFillState method [GDI+], SetFillState method [GDI+],AdjustableArrowCap class, _gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_, gdiplus._gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_
req.header: gdipluslinecaps.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - AdjustableArrowCap::SetFillState
 - gdipluslinecaps/AdjustableArrowCap::SetFillState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - AdjustableArrowCap.SetFillState
---

# AdjustableArrowCap::SetFillState


## -description

The <b>AdjustableArrowCap::SetFillState</b> method sets the fill state of the arrow cap. If the arrow cap is not filled, only the outline is drawn.

## -parameters

### -param isFilled [in]

Type: <b>BOOL</b>

Boolean value that specifies whether the arrow cap is filled.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.