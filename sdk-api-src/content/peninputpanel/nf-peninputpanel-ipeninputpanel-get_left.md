---
UID: NF:peninputpanel.IPenInputPanel.get_Left
title: IPenInputPanel::get_Left (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the horizontal, or x-axis, location of the left edge of the PenInputPanel object, in screen coordinates.
helpviewer_keywords: ["99af3767-5bc9-43e3-9413-5886f057cb85","IPenInputPanel interface [Tablet PC]","Left property","IPenInputPanel.Left","IPenInputPanel.get_Left","IPenInputPanel::Left","IPenInputPanel::get_Left","Left property [Tablet PC]","Left property [Tablet PC]","IPenInputPanel interface","PenInputPanel.get_Left","get_Left","peninputpanel/IPenInputPanel::Left","peninputpanel/IPenInputPanel::get_Left","tablet.peninputpanel_left"]
old-location: tablet\peninputpanel_left.htm
tech.root: tablet
ms.assetid: 99af3767-5bc9-43e3-9413-5886f057cb85
ms.date: 12/05/2018
ms.keywords: 99af3767-5bc9-43e3-9413-5886f057cb85, IPenInputPanel interface [Tablet PC],Left property, IPenInputPanel.Left, IPenInputPanel.get_Left, IPenInputPanel::Left, IPenInputPanel::get_Left, Left property [Tablet PC], Left property [Tablet PC],IPenInputPanel interface, PenInputPanel.get_Left, get_Left, peninputpanel/IPenInputPanel::Left, peninputpanel/IPenInputPanel::get_Left, tablet.peninputpanel_left
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
 - IPenInputPanel::get_Left
 - peninputpanel/IPenInputPanel::get_Left
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
 - IPenInputPanel.Left
 - IPenInputPanel.get_Left
 - PenInputPanel.get_Left
---

# IPenInputPanel::get_Left


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the horizontal, or x-axis, location of the left edge of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, in screen coordinates.



This property is read-only.

## -parameters

## -remarks

To explicitly override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, use the <b>Left</b> and <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top">Top</a> properties of the object to determine the current position of the pen input panel. If the pen input panel is located on a section of the screen that should be visible, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto">MoveTo</a> method to relocate the pen input panel.

You can also override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object by listening for the <i>Left</i> and <i>Top</i> parameters during a <a href="/windows/desktop/tablet/peninputpanel-panelmoving">PanelMoving</a> event. If the pen input panel is located on a section of the screen that should be visible, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto">MoveTo</a> method to relocate the pen input panel.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top">Top Property [PenInputPanel Class]</a>
