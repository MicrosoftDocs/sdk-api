---
UID: NF:peninputpanel.IPenInputPanel.get_HorizontalOffset
title: IPenInputPanel::get_HorizontalOffset (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached.helpviewer_keywords: ["835b9d08-871a-4a28-8b10-c9a0e8829674","HorizontalOffset property [Tablet PC]","HorizontalOffset property [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","HorizontalOffset property","IPenInputPanel.HorizontalOffset","IPenInputPanel.get_HorizontalOffset","IPenInputPanel::HorizontalOffset","IPenInputPanel::get_HorizontalOffset","IPenInputPanel::put_HorizontalOffset","PenInputPanel.get_HorizontalOffset","PenInputPanel.put_HorizontalOffset","get_HorizontalOffset","peninputpanel/IPenInputPanel::HorizontalOffset","peninputpanel/IPenInputPanel::get_HorizontalOffset","peninputpanel/IPenInputPanel::put_HorizontalOffset","put_HorizontalOffset","tablet.peninputpanel_horizontaloffset"]
old-location: tablet\peninputpanel_horizontaloffset.htm
tech.root: tablet
ms.assetid: 835b9d08-871a-4a28-8b10-c9a0e8829674
ms.date: 12/05/2018
ms.keywords: 835b9d08-871a-4a28-8b10-c9a0e8829674, HorizontalOffset property [Tablet PC], HorizontalOffset property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],HorizontalOffset property, IPenInputPanel.HorizontalOffset, IPenInputPanel.get_HorizontalOffset, IPenInputPanel::HorizontalOffset, IPenInputPanel::get_HorizontalOffset, IPenInputPanel::put_HorizontalOffset, PenInputPanel.get_HorizontalOffset, PenInputPanel.put_HorizontalOffset, get_HorizontalOffset, peninputpanel/IPenInputPanel::HorizontalOffset, peninputpanel/IPenInputPanel::get_HorizontalOffset, peninputpanel/IPenInputPanel::put_HorizontalOffset, put_HorizontalOffset, tablet.peninputpanel_horizontaloffset
f1_keywords:
- peninputpanel/IPenInputPanel.HorizontalOffset
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPenInputPanel::get_HorizontalOffset


## -description



Deprecated.  The <a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="https://docs.microsoft.com/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached.



This property is read/write.


## -parameters


## -remarks



The default value is the equivalent of 0.25 inches in pixels, dependent on screen resolution settings. A negative value indicates a shift to the left of the control. A positive value indicates a shift to the right. A zero value indicates that the left edge of the pen input panel is positioned exactly at the left edge of the control.

If the new position causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846809(v=VS.85).aspx">IPenInputPanel</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset">VerticalOffset Property</a>
 

 

