---
UID: NF:peninputpanel.IPenInputPanel.MoveTo
title: IPenInputPanel::MoveTo (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sets the position of the PenInputPanel object to a static screen position.
helpviewer_keywords: ["IPenInputPanel interface [Tablet PC]","MoveTo method","IPenInputPanel.MoveTo","IPenInputPanel::MoveTo","MoveTo","MoveTo method [Tablet PC]","MoveTo method [Tablet PC]","IPenInputPanel interface","d99e5ef8-fa91-4507-bfe5-f30a039ca72d","peninputpanel/IPenInputPanel::MoveTo","tablet.peninputpanel_moveto"]
old-location: tablet\peninputpanel_moveto.htm
tech.root: tablet
ms.assetid: d99e5ef8-fa91-4507-bfe5-f30a039ca72d
ms.date: 12/05/2018
ms.keywords: IPenInputPanel interface [Tablet PC],MoveTo method, IPenInputPanel.MoveTo, IPenInputPanel::MoveTo, MoveTo, MoveTo method [Tablet PC], MoveTo method [Tablet PC],IPenInputPanel interface, d99e5ef8-fa91-4507-bfe5-f30a039ca72d, peninputpanel/IPenInputPanel::MoveTo, tablet.peninputpanel_moveto
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
 - IPenInputPanel::MoveTo
 - peninputpanel/IPenInputPanel::MoveTo
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
 - IPenInputPanel.MoveTo
---

# IPenInputPanel::MoveTo


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Sets the position of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object to a static screen position.

## -parameters

### -param Left [in]

 The new horizontal position in screen coordinates.

### -param Top [in]

The new vertical position in screen coordinates.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

The <b>MoveTo</b> method causes an error if the control to which the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> is attached does not have focus. This method can be safely called if the pen input panel is not visible, as long as the attached control has focus.

If the new position causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.

To explicitly override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, use the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left">Left</a> and <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top">Top</a> properties of the <b>PenInputPanel</b> object to determine its current position. If the <b>PenInputPanel</b> is located on a section of the screen that should be visible, use the <b>MoveTo</b> method to relocate the <b>PenInputPanel</b>.

You can also override the automatic positioning behavior of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object by monitoring to the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left">Left</a> and <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top">Top</a> parameters passed to a <a href="/windows/desktop/tablet/peninputpanel-panelmoving">PanelMoving</a> event handler. If the <b>PenInputPanel</b> is located on a section of the screen that should be visible, use the <b>MoveTo</b> method to relocate the <b>PenInputPanel</b>.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
