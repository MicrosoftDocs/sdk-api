---
UID: NF:peninputpanel.IPenInputPanel.get_VerticalOffset
title: IPenInputPanel::get_VerticalOffset (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the closest horizontal edge of the pen input panel and the closest horizontal edge of the control to which it is attached. (IPenInputPanel.get_VerticalOffset)
helpviewer_keywords: ["IPenInputPanel interface [Tablet PC]","VerticalOffset property","IPenInputPanel.VerticalOffset","IPenInputPanel.get_VerticalOffset","IPenInputPanel::VerticalOffset","IPenInputPanel::get_VerticalOffset","IPenInputPanel::put_VerticalOffset","PenInputPanel.get_VerticalOffset","PenInputPanel.put_VerticalOffset","VerticalOffset property [Tablet PC]","VerticalOffset property [Tablet PC]","IPenInputPanel interface","ad4b00cc-5cb5-4c32-b837-b13a699ae7e6","get_VerticalOffset","peninputpanel/IPenInputPanel::VerticalOffset","peninputpanel/IPenInputPanel::get_VerticalOffset","peninputpanel/IPenInputPanel::put_VerticalOffset","put_VerticalOffset","tablet.peninputpanel_verticaloffset"]
old-location: tablet\peninputpanel_verticaloffset.htm
tech.root: tablet
ms.assetid: ad4b00cc-5cb5-4c32-b837-b13a699ae7e6
ms.date: 12/05/2018
ms.keywords: IPenInputPanel interface [Tablet PC],VerticalOffset property, IPenInputPanel.VerticalOffset, IPenInputPanel.get_VerticalOffset, IPenInputPanel::VerticalOffset, IPenInputPanel::get_VerticalOffset, IPenInputPanel::put_VerticalOffset, PenInputPanel.get_VerticalOffset, PenInputPanel.put_VerticalOffset, VerticalOffset property [Tablet PC], VerticalOffset property [Tablet PC],IPenInputPanel interface, ad4b00cc-5cb5-4c32-b837-b13a699ae7e6, get_VerticalOffset, peninputpanel/IPenInputPanel::VerticalOffset, peninputpanel/IPenInputPanel::get_VerticalOffset, peninputpanel/IPenInputPanel::put_VerticalOffset, put_VerticalOffset, tablet.peninputpanel_verticaloffset
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPenInputPanel::get_VerticalOffset
 - peninputpanel/IPenInputPanel::get_VerticalOffset
dev_langs:
 - c++
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
---

# IPenInputPanel::get_VerticalOffset


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the offset between the closest horizontal edge of the pen input panel  and the closest horizontal edge of the control to which it is attached.



This property is read/write.

## -parameters

## -remarks

The default value is the equivalent of 1/16 inches in pixels, dependent on screen resolution settings. A value of 0 (zero) attaches the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object directly to the bottom of the control. A value of -1 places it 1 pixel above the control.

If the new position of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset">HorizontalOffset Property</a>



<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
