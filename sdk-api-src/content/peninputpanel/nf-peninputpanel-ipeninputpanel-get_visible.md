---
UID: NF:peninputpanel.IPenInputPanel.get_Visible
title: IPenInputPanel::get_Visible (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets a value that indicates whether the PenInputPanel object is visible.
helpviewer_keywords: ["561b1a92-2e7e-4e8a-8fad-ebb515328cb7","IPenInputPanel interface [Tablet PC]","Visible property","IPenInputPanel.Visible","IPenInputPanel.get_Visible","IPenInputPanel::Visible","IPenInputPanel::get_Visible","IPenInputPanel::putref_Visible","PenInputPanel.get_Visible","Visible property [Tablet PC]","Visible property [Tablet PC]","IPenInputPanel interface","get_Visible","peninputpanel/IPenInputPanel::Visible","peninputpanel/IPenInputPanel::get_Visible","peninputpanel/IPenInputPanel::putref_Visible","put_Visible","tablet.peninputpanel_visible"]
old-location: tablet\peninputpanel_visible.htm
tech.root: tablet
ms.assetid: 561b1a92-2e7e-4e8a-8fad-ebb515328cb7
ms.date: 12/05/2018
ms.keywords: 561b1a92-2e7e-4e8a-8fad-ebb515328cb7, IPenInputPanel interface [Tablet PC],Visible property, IPenInputPanel.Visible, IPenInputPanel.get_Visible, IPenInputPanel::Visible, IPenInputPanel::get_Visible, IPenInputPanel::putref_Visible, PenInputPanel.get_Visible, Visible property [Tablet PC], Visible property [Tablet PC],IPenInputPanel interface, get_Visible, peninputpanel/IPenInputPanel::Visible, peninputpanel/IPenInputPanel::get_Visible, peninputpanel/IPenInputPanel::putref_Visible, put_Visible, tablet.peninputpanel_visible
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
 - IPenInputPanel::get_Visible
 - peninputpanel/IPenInputPanel::get_Visible
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
 - IPenInputPanel.Visible
 - IPenInputPanel.get_Visible
 - PenInputPanel.get_Visible
---

# IPenInputPanel::get_Visible


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets a value that indicates whether the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is visible.



This property is read/write.

## -parameters

## -remarks

You can set the <b>Visible</b> property to <b>VARIANT_TRUE</b> only when the attached control has focus. Otherwise, setting this property generates an error.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
