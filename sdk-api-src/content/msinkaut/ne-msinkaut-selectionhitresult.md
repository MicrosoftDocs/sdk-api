---
UID: NE:msinkaut.SelectionHitResult
title: SelectionHitResult (msinkaut.h)
description: Specifies which part of a selection, if any, was hit during a hit test.
helpviewer_keywords: ["SHR_E","SHR_N","SHR_NE","SHR_NW","SHR_None","SHR_S","SHR_SE","SHR_SW","SHR_Selection","SHR_W","SelectionHitResult","SelectionHitResult enumeration [Tablet PC]","a93d0121-e271-4656-9cdc-ae05fd19ac8b","msinkaut/SHR_E","msinkaut/SHR_N","msinkaut/SHR_NE","msinkaut/SHR_NW","msinkaut/SHR_None","msinkaut/SHR_S","msinkaut/SHR_SE","msinkaut/SHR_SW","msinkaut/SHR_Selection","msinkaut/SHR_W","msinkaut/SelectionHitResult","tablet.selectionhitresult"]
old-location: tablet\selectionhitresult.htm
tech.root: tablet
ms.assetid: a93d0121-e271-4656-9cdc-ae05fd19ac8b
ms.date: 12/05/2018
ms.keywords: SHR_E, SHR_N, SHR_NE, SHR_NW, SHR_None, SHR_S, SHR_SE, SHR_SW, SHR_Selection, SHR_W, SelectionHitResult, SelectionHitResult enumeration [Tablet PC], a93d0121-e271-4656-9cdc-ae05fd19ac8b, msinkaut/SHR_E, msinkaut/SHR_N, msinkaut/SHR_NE, msinkaut/SHR_NW, msinkaut/SHR_None, msinkaut/SHR_S, msinkaut/SHR_SE, msinkaut/SHR_SW, msinkaut/SHR_Selection, msinkaut/SHR_W, msinkaut/SelectionHitResult, tablet.selectionhitresult
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.typenames: SelectionHitResult
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SelectionHitResult
 - msinkaut/SelectionHitResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - SelectionHitResult
---

# SelectionHitResult enumeration


## -description

Specifies which part of a selection, if any, was hit during a hit test.

## -enum-fields

### -field SHR_None:0

No part of the selection was hit.

### -field SHR_NW

The northwest corner sizing handle was hit.

### -field SHR_SE

The southeast corner sizing handle was hit.

### -field SHR_NE

The northeast corner sizing handle was hit.

### -field SHR_SW

That the southwest corner sizing handle was hit.

### -field SHR_E

The east side sizing handle was hit.

### -field SHR_W

The west side sizing handle was hit.

### -field SHR_N

The north side sizing handle was hit.

### -field SHR_S

The south side sizing handle was hit.

### -field SHR_Selection

The selection itself was hit (no selection handle was hit).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection">HitTestSelection Method [InkOverlay Class]</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>
