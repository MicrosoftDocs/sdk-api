---
UID: NE:msinkaut.InkShiftKeyModifierFlags
title: InkShiftKeyModifierFlags (msinkaut.h)
description: Specifies which modifier key was pressed.
helpviewer_keywords: ["03c2e5d4-fcba-4b6c-9982-54b451ef129d","IKM_Alt","IKM_Control","IKM_Shift","InkShiftKeyModifierFlags","InkShiftKeyModifierFlags enumeration [Tablet PC]","msinkaut/IKM_Alt","msinkaut/IKM_Control","msinkaut/IKM_Shift","msinkaut/InkShiftKeyModifierFlags","tablet.inkshiftkeymodifierflags"]
old-location: tablet\inkshiftkeymodifierflags.htm
tech.root: tablet
ms.assetid: 03c2e5d4-fcba-4b6c-9982-54b451ef129d
ms.date: 12/05/2018
ms.keywords: 03c2e5d4-fcba-4b6c-9982-54b451ef129d, IKM_Alt, IKM_Control, IKM_Shift, InkShiftKeyModifierFlags, InkShiftKeyModifierFlags enumeration [Tablet PC], msinkaut/IKM_Alt, msinkaut/IKM_Control, msinkaut/IKM_Shift, msinkaut/InkShiftKeyModifierFlags, tablet.inkshiftkeymodifierflags
f1_keywords:
- msinkaut/InkShiftKeyModifierFlags
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
- InkShiftKeyModifierFlags
targetos: Windows
req.typenames: InkShiftKeyModifierFlags
req.redist: 
ms.custom: 19H1
---

# InkShiftKeyModifierFlags enumeration


## -description



Specifies which modifier key was pressed.




## -enum-fields




### -field IKM_Shift

The SHIFT key was used as a modifier.


### -field IKM_Control

The CTRL key was used as a modifier.


### -field IKM_Alt

The ALT key was used as a modifier.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-keydown">KeyDown Event [InkEdit Control]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-keyup">KeyUp Event [InkEdit Control]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-mousedown">MouseDown Event [InkPicture Control]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-mousemove">MouseMove Event [InkPicture Control]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-mouseup">MouseUp Event [InkOverlay Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-mousewheel">MouseWheel Event [InkPicture Control]</a>
 

 

