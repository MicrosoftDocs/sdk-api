---
UID: NF:peninputpanel.IPenInputPanel.get_Top
title: IPenInputPanel::get_Top
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the vertical, or y-axis, location of the top edge of the PenInputPanel object, in screen coordinates.
old-location: tablet\peninputpanel_top.htm
old-project: tablet
ms.assetid: 718263ae-d6ba-47ec-a18b-50488480b599
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 718263ae-d6ba-47ec-a18b-50488480b599, Get_Top, IPenInputPanel interface [Tablet PC],Top property, IPenInputPanel.Top, IPenInputPanel.get_Top, IPenInputPanel::Top, IPenInputPanel::get_Top, PenInputPanel.get_Top, Top property [Tablet PC], Top property [Tablet PC],IPenInputPanel interface, get_Top, peninputpanel/IPenInputPanel::Top, peninputpanel/IPenInputPanel::get_Top, tablet.peninputpanel_top
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IPenInputPanel.Top
-	IPenInputPanel.get_Top
-	PenInputPanel.get_Top
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPenInputPanel::get_Top


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets the vertical, or y-axis, location of the top edge of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, in screen coordinates.



This property is read-only.


## -parameters


## -remarks



To explicitly override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, use the <a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left</a> and <b>Top</b> properties of the object to determine the current position of the pen input panel. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.

You can also override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object by listening for the <i>Left</i> and <i>Top</i> parameters during a <a href="https://msdn.microsoft.com/0c51d875-cef9-4087-b17d-5c5af04f81a5">PanelMoving</a> event. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.




## -see-also




<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left Property [PenInputPanel Class]</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

