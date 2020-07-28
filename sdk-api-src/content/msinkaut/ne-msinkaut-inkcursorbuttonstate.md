---
UID: NE:msinkaut.InkCursorButtonState
title: InkCursorButtonState (msinkaut.h)
description: Defines values that specify the state of a cursor button.
helpviewer_keywords: ["0e750bd6-0b57-499e-9691-966fb027cdb5","ICBS_CursorUnavailable","ICBS_Down","ICBS_Up","InkCursorButtonState","InkCursorButtonState enumeration [Tablet PC]","msinkaut/ICBS_CursorUnavailable","msinkaut/ICBS_Down","msinkaut/ICBS_Up","msinkaut/InkCursorButtonState","tablet.inkcursorbuttonstate"]
old-location: tablet\inkcursorbuttonstate.htm
tech.root: tablet
ms.assetid: 0e750bd6-0b57-499e-9691-966fb027cdb5
ms.date: 12/05/2018
ms.keywords: 0e750bd6-0b57-499e-9691-966fb027cdb5, ICBS_CursorUnavailable, ICBS_Down, ICBS_Up, InkCursorButtonState, InkCursorButtonState enumeration [Tablet PC], msinkaut/ICBS_CursorUnavailable, msinkaut/ICBS_Down, msinkaut/ICBS_Up, msinkaut/InkCursorButtonState, tablet.inkcursorbuttonstate
f1_keywords:
- msinkaut/InkCursorButtonState
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- msinkaut.h
api_name:
- InkCursorButtonState
targetos: Windows
req.typenames: InkCursorButtonState
req.redist: 
ms.custom: 19H1
---

# InkCursorButtonState enumeration


## -description



Defines values that specify the state of a cursor button.




## -enum-fields




### -field ICBS_Unavailable


### -field ICBS_Up

The cursor button is up. A button on a pen tip is up when the pen is not pressed against the digitizer. A button on a pen barrel is up when the button is not depressed.


### -field ICBS_Down

The cursor button is down. A button on a pen tip is down when the user lowers the pen to the digitizer and draws a stroke. For a button on a barrel, the button is down when the button is depressed.


#### - ICBS_CursorUnavailable

The cursor button is unavailable. A cursor button may become unavailable, for example, when a cursor leaves the range of Tablet PC.


## -remarks



The CursorButton state for the mouse is always <b>CursorUnavailable</b> when the mouse buttons are up.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange Event</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursorbutton-get_state">State Property</a>
 

 

