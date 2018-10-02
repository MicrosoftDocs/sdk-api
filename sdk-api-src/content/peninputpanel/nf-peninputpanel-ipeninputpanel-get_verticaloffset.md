---
UID: NF:peninputpanel.IPenInputPanel.get_VerticalOffset
title: IPenInputPanel::get_VerticalOffset
author: windows-sdk-content
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the closest horizontal edge of the pen input panel and the closest horizontal edge of the control to which it is attached.
old-location: tablet\peninputpanel_verticaloffset.htm
tech.root: tablet
ms.assetid: ad4b00cc-5cb5-4c32-b837-b13a699ae7e6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IPenInputPanel interface [Tablet PC],VerticalOffset property, IPenInputPanel.VerticalOffset, IPenInputPanel.get_VerticalOffset, IPenInputPanel::VerticalOffset, IPenInputPanel::get_VerticalOffset, IPenInputPanel::put_VerticalOffset, PenInputPanel.get_VerticalOffset, PenInputPanel.put_VerticalOffset, VerticalOffset property [Tablet PC], VerticalOffset property [Tablet PC],IPenInputPanel interface, ad4b00cc-5cb5-4c32-b837-b13a699ae7e6, get_VerticalOffset, peninputpanel/IPenInputPanel::VerticalOffset, peninputpanel/IPenInputPanel::get_VerticalOffset, peninputpanel/IPenInputPanel::put_VerticalOffset, put_VerticalOffset, tablet.peninputpanel_verticaloffset
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPenInputPanel.VerticalOffset
 - IPenInputPanel.get_VerticalOffset
 - IPenInputPanel.put_VerticalOffset
 - PenInputPanel.get_VerticalOffset
 - PenInputPanel.put_VerticalOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPenInputPanel::get_VerticalOffset


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets or sets the offset between the closest horizontal edge of the pen input panel  and the closest horizontal edge of the control to which it is attached.



This property is read/write.


## -parameters


## -remarks



The default value is the equivalent of 1/16 inches in pixels, dependent on screen resolution settings. A value of 0 (zero) attaches the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object directly to the bottom of the control. A value of -1 places it 1 pixel above the control.

If the new position of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.




## -see-also




<a href="https://msdn.microsoft.com/835b9d08-871a-4a28-8b10-c9a0e8829674">HorizontalOffset Property</a>



<a href="https://msdn.microsoft.com/AA973F9D-264F-4D08-9D86-C5DAEF1C09D5">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

