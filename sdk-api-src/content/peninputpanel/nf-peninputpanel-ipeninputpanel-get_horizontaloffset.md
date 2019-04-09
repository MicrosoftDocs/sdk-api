---
UID: NF:peninputpanel.IPenInputPanel.get_HorizontalOffset
title: IPenInputPanel::get_HorizontalOffset (peninputpanel.h)
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached.
old-location: tablet\peninputpanel_horizontaloffset.htm
tech.root: tablet
ms.assetid: 835b9d08-871a-4a28-8b10-c9a0e8829674
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 835b9d08-871a-4a28-8b10-c9a0e8829674, HorizontalOffset property [Tablet PC], HorizontalOffset property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],HorizontalOffset property, IPenInputPanel.HorizontalOffset, IPenInputPanel.get_HorizontalOffset, IPenInputPanel::HorizontalOffset, IPenInputPanel::get_HorizontalOffset, IPenInputPanel::put_HorizontalOffset, PenInputPanel.get_HorizontalOffset, PenInputPanel.put_HorizontalOffset, get_HorizontalOffset, peninputpanel/IPenInputPanel::HorizontalOffset, peninputpanel/IPenInputPanel::get_HorizontalOffset, peninputpanel/IPenInputPanel::put_HorizontalOffset, put_HorizontalOffset, tablet.peninputpanel_horizontaloffset
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.HorizontalOffset
 - IPenInputPanel.get_HorizontalOffset
 - IPenInputPanel.put_HorizontalOffset
 - PenInputPanel.get_HorizontalOffset
 - PenInputPanel.put_HorizontalOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::get_HorizontalOffset


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached.



This property is read/write.


## -parameters


## -remarks



The default value is the equivalent of 0.25 inches in pixels, dependent on screen resolution settings. A negative value indicates a shift to the left of the control. A positive value indicates a shift to the right. A zero value indicates that the left edge of the pen input panel is positioned exactly at the left edge of the control.

If the new position causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846809(v=VS.85).aspx">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>



<a href="https://msdn.microsoft.com/ad4b00cc-5cb5-4c32-b837-b13a699ae7e6">VerticalOffset Property</a>
 

 

