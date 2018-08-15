---
UID: NE:msinkaut.SelectionHitResult
title: SelectionHitResult
author: windows-sdk-content
description: Specifies which part of a selection, if any, was hit during a hit test.
old-location: tablet\selectionhitresult.htm
old-project: tablet
ms.assetid: a93d0121-e271-4656-9cdc-ae05fd19ac8b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHR_E, SHR_N, SHR_NE, SHR_NW, SHR_None, SHR_S, SHR_SE, SHR_SW, SHR_Selection, SHR_W, SelectionHitResult, SelectionHitResult enumeration [Tablet PC], a93d0121-e271-4656-9cdc-ae05fd19ac8b, msinkaut/SHR_E, msinkaut/SHR_N, msinkaut/SHR_NE, msinkaut/SHR_NW, msinkaut/SHR_None, msinkaut/SHR_S, msinkaut/SHR_SE, msinkaut/SHR_SW, msinkaut/SHR_Selection, msinkaut/SHR_W, msinkaut/SelectionHitResult, tablet.selectionhitresult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SelectionHitResult
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - SelectionHitResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SelectionHitResult enumeration


## -description



Specifies which part of a selection, if any, was hit during a hit test.




## -enum-fields




### -field SHR_None

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




<a href="https://msdn.microsoft.com/289589fa-84da-40b3-b60e-551ef0114279">HitTestSelection Method [InkOverlay Class]</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>
 

 

