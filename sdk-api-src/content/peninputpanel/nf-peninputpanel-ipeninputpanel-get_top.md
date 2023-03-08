---
UID: NF:peninputpanel.IPenInputPanel.get_Top
title: IPenInputPanel::get_Top (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the vertical, or y-axis, location of the top edge of the PenInputPanel object, in screen coordinates.
helpviewer_keywords: ["718263ae-d6ba-47ec-a18b-50488480b599","Get_Top","IPenInputPanel interface [Tablet PC]","Top property","IPenInputPanel.Top","IPenInputPanel.get_Top","IPenInputPanel::Top","IPenInputPanel::get_Top","PenInputPanel.get_Top","Top property [Tablet PC]","Top property [Tablet PC]","IPenInputPanel interface","get_Top","peninputpanel/IPenInputPanel::Top","peninputpanel/IPenInputPanel::get_Top","tablet.peninputpanel_top"]
old-location: tablet\peninputpanel_top.htm
tech.root: tablet
ms.assetid: 718263ae-d6ba-47ec-a18b-50488480b599
ms.date: 12/05/2018
ms.keywords: 718263ae-d6ba-47ec-a18b-50488480b599, Get_Top, IPenInputPanel interface [Tablet PC],Top property, IPenInputPanel.Top, IPenInputPanel.get_Top, IPenInputPanel::Top, IPenInputPanel::get_Top, PenInputPanel.get_Top, Top property [Tablet PC], Top property [Tablet PC],IPenInputPanel interface, get_Top, peninputpanel/IPenInputPanel::Top, peninputpanel/IPenInputPanel::get_Top, tablet.peninputpanel_top
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
 - IPenInputPanel::get_Top
 - peninputpanel/IPenInputPanel::get_Top
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
 - IPenInputPanel.Top
 - IPenInputPanel.get_Top
 - PenInputPanel.get_Top
---

# IPenInputPanel::get_Top


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the vertical, or y-axis, location of the top edge of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, in screen coordinates.



This property is read-only.

## -parameters

## -remarks

To explicitly override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left">Left</a> and <b>Top</b> properties of the object to determine the current position of the pen input panel. If the pen input panel is located on a section of the screen that should be visible, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto">MoveTo</a> method to relocate the pen input panel.

You can also override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object by listening for the <i>Left</i> and <i>Top</i> parameters during a <a href="/windows/desktop/tablet/peninputpanel-panelmoving">PanelMoving</a> event. If the pen input panel is located on a section of the screen that should be visible, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto">MoveTo</a> method to relocate the pen input panel.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left">Left Property [PenInputPanel Class]</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
