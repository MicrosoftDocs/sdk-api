---
UID: NF:peninputpanel.IPenInputPanel.put_CurrentPanel
title: IPenInputPanel::put_CurrentPanel (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets which panel type is currently being used for input within the PenInputPanel object. (IPenInputPanel.put_CurrentPanel)
helpviewer_keywords: ["536ba874-b9f9-45c9-bf9a-a64679afc861","CurrentPanel property [Tablet PC]","CurrentPanel property [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","CurrentPanel property","IPenInputPanel.CurrentPanel","IPenInputPanel.put_CurrentPanel","IPenInputPanel::CurrentPanel","IPenInputPanel::get_CurrentPanel","IPenInputPanel::put_CurrentPanel","PenInputPanel.get_CurrentPanel","PenInputPanel.put_CurrentPanel","get_CurrentPanel","peninputpanel/IPenInputPanel::CurrentPanel","peninputpanel/IPenInputPanel::get_CurrentPanel","peninputpanel/IPenInputPanel::put_CurrentPanel","put_CurrentPanel","tablet.peninputpanel_currentpanel"]
old-location: tablet\peninputpanel_currentpanel.htm
tech.root: tablet
ms.assetid: 536ba874-b9f9-45c9-bf9a-a64679afc861
ms.date: 12/05/2018
ms.keywords: 536ba874-b9f9-45c9-bf9a-a64679afc861, CurrentPanel property [Tablet PC], CurrentPanel property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],CurrentPanel property, IPenInputPanel.CurrentPanel, IPenInputPanel.put_CurrentPanel, IPenInputPanel::CurrentPanel, IPenInputPanel::get_CurrentPanel, IPenInputPanel::put_CurrentPanel, PenInputPanel.get_CurrentPanel, PenInputPanel.put_CurrentPanel, get_CurrentPanel, peninputpanel/IPenInputPanel::CurrentPanel, peninputpanel/IPenInputPanel::get_CurrentPanel, peninputpanel/IPenInputPanel::put_CurrentPanel, put_CurrentPanel, tablet.peninputpanel_currentpanel
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
 - IPenInputPanel::put_CurrentPanel
 - peninputpanel/IPenInputPanel::put_CurrentPanel
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
 - IPenInputPanel.CurrentPanel
 - IPenInputPanel.get_CurrentPanel
 - IPenInputPanel.put_CurrentPanel
 - PenInputPanel.get_CurrentPanel
 - PenInputPanel.put_CurrentPanel
---

# IPenInputPanel::put_CurrentPanel


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets which panel type is currently being used for input within the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The <b>CurrentPanel</b> property cannot be set to <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Default</a> or <b>Inactive</b>, only <b>Handwriting</b> or <b>Keyboard</b>.</div>
<div> </div>
When you create a <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, the <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Handwriting</a> panel - also known as the writing pad - is the default input UI.

If you change the panel by setting the <b>CurrentPanel</b> property before the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object becomes active for the first time, a <a href="/windows/desktop/tablet/peninputpanel-panelchanged">PanelChanged</a> event occurs.

<b>CurrentPanel</b> returns the <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Inactive</a> enumeration value if the panel window is associated with another instance of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object. Setting the <b>CurrentPanel</b> property raises an exception if the panel is inactive or if the panel type is invalid.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel">DefaultPanel Property</a>



<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">PanelType Enumeration</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
