---
UID: NF:peninputpanel.IPenInputPanel.get_Left
title: IPenInputPanel::get_Left
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the horizontal, or x-axis, location of the left edge of the PenInputPanel object, in screen coordinates.
old-location: tablet\peninputpanel_left.htm
old-project: tablet
ms.assetid: 99af3767-5bc9-43e3-9413-5886f057cb85
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 99af3767-5bc9-43e3-9413-5886f057cb85, IPenInputPanel interface [Tablet PC],Left property, IPenInputPanel.Left, IPenInputPanel.get_Left, IPenInputPanel::Left, IPenInputPanel::get_Left, Left property [Tablet PC], Left property [Tablet PC],IPenInputPanel interface, PenInputPanel.get_Left, get_Left, peninputpanel/IPenInputPanel::Left, peninputpanel/IPenInputPanel::get_Left, tablet.peninputpanel_left
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: peninputpanel.h
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.Left
 - IPenInputPanel.get_Left
 - PenInputPanel.get_Left
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: ADAM
---

# IPenInputPanel::get_Left


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets the horizontal, or x-axis, location of the left edge of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, in screen coordinates.



This property is read-only.


## -parameters


## -remarks



To explicitly override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, use the <b>Left</b> and <a href="https://msdn.microsoft.com/718263ae-d6ba-47ec-a18b-50488480b599">Top</a> properties of the object to determine the current position of the pen input panel. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.

You can also override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object by listening for the <i>Left</i> and <i>Top</i> parameters during a <a href="https://msdn.microsoft.com/0c51d875-cef9-4087-b17d-5c5af04f81a5">PanelMoving</a> event. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.




## -see-also




<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>



<a href="https://msdn.microsoft.com/718263ae-d6ba-47ec-a18b-50488480b599">Top Property [PenInputPanel Class]</a>
 

 

