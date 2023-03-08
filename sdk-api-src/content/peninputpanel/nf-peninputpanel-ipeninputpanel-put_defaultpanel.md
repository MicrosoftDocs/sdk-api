---
UID: NF:peninputpanel.IPenInputPanel.put_DefaultPanel
title: IPenInputPanel::put_DefaultPanel (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the default panel type used for input within the PenInputPanel object. (Put)
helpviewer_keywords: ["2b0ff320-02ce-4b23-ae47-91504c93ac24","DefaultPanel property [Tablet PC]","DefaultPanel property [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","DefaultPanel property","IPenInputPanel.DefaultPanel","IPenInputPanel.put_DefaultPanel","IPenInputPanel::DefaultPanel","IPenInputPanel::get_DefaultPanel","IPenInputPanel::put_DefaultPanel","PenInputPanel.get_DefaultPanel","PenInputPanel.put_DefaultPanel","get_DefaultPanel","peninputpanel/IPenInputPanel::DefaultPanel","peninputpanel/IPenInputPanel::get_DefaultPanel","peninputpanel/IPenInputPanel::put_DefaultPanel","put_DefaultPanel","tablet.peninputpanel_defaultpanel"]
old-location: tablet\peninputpanel_defaultpanel.htm
tech.root: tablet
ms.assetid: 2b0ff320-02ce-4b23-ae47-91504c93ac24
ms.date: 12/05/2018
ms.keywords: 2b0ff320-02ce-4b23-ae47-91504c93ac24, DefaultPanel property [Tablet PC], DefaultPanel property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],DefaultPanel property, IPenInputPanel.DefaultPanel, IPenInputPanel.put_DefaultPanel, IPenInputPanel::DefaultPanel, IPenInputPanel::get_DefaultPanel, IPenInputPanel::put_DefaultPanel, PenInputPanel.get_DefaultPanel, PenInputPanel.put_DefaultPanel, get_DefaultPanel, peninputpanel/IPenInputPanel::DefaultPanel, peninputpanel/IPenInputPanel::get_DefaultPanel, peninputpanel/IPenInputPanel::put_DefaultPanel, put_DefaultPanel, tablet.peninputpanel_defaultpanel
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
 - IPenInputPanel::put_DefaultPanel
 - peninputpanel/IPenInputPanel::put_DefaultPanel
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
 - IPenInputPanel.DefaultPanel
 - IPenInputPanel.get_DefaultPanel
 - IPenInputPanel.put_DefaultPanel
 - PenInputPanel.get_DefaultPanel
 - PenInputPanel.put_DefaultPanel
---

# IPenInputPanel::put_DefaultPanel


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets the default panel type used for input within the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The <b>DefaultPanel</b> property cannot be set to <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Inactive</a>.</div>
<div> </div>
The <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Handwriting</a> panel-also known as the writing pad-is the default input UI for a <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>.

If the value of this property is <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Default</a>, then the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object uses the last panel type used for any pen input panel in any application. If all previous references to the pen input panel have been destroyed in all active applications, a new <b>PenInputPanel</b> object uses the <b>Handwriting</b> panel type.

If the panel is changed by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel</a> property before the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object becomes active for the first time, a <a href="/windows/desktop/tablet/peninputpanel-panelchanged">PanelChanged</a> event occurs.

Setting the <b>DefaultPanel</b> property enables you to specify which type of panel shows by default in that instance of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object. If the value of this property is <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Handwriting</a> or <b>Keyboard</b>, then each time the panel is made visible, it uses the handwriting or keyboard panel type, respectively.

If you re-attach the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> to a different control and change the <b>DefaultPanel</b> property when the focus changes to the new control, be sure to set the <b>DefaultPanel</b> property before setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow">AttachedEditWindow</a> property to ensure that the correct panel is displayed.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel Property</a>



<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">PanelType Enumeration</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
