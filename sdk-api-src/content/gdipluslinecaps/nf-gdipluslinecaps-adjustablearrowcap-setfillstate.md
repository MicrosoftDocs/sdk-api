---
UID: NF:gdipluslinecaps.AdjustableArrowCap.SetFillState
title: AdjustableArrowCap::SetFillState
author: windows-sdk-content
description: The AdjustableArrowCap::SetFillState method sets the fill state of the arrow cap. If the arrow cap is not filled, only the outline is drawn.
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcapclass\adjustablearrowcapmethods\setfillstate.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AdjustableArrowCap class [GDI+],SetFillState method, AdjustableArrowCap.SetFillState, AdjustableArrowCap::SetFillState, SetFillState, SetFillState method [GDI+], SetFillState method [GDI+],AdjustableArrowCap class, _gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_, gdiplus._gdiplus_CLASS_AdjustableArrowCap_SetFillState_isFilled_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - AdjustableArrowCap.SetFillState
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# AdjustableArrowCap::SetFillState


## -description


The <b>AdjustableArrowCap::SetFillState</b> method sets the fill state of the arrow cap. If the arrow cap is not filled, only the outline is drawn.


## -parameters




### -param isFilled [in]

Type: <b>BOOL</b>

Boolean value that specifies whether the arrow cap is filled. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.



