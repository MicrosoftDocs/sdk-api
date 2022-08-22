---
UID: NF:peninputpanel.IPenInputPanel.put_AutoShow
title: IPenInputPanel::put_AutoShow (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets a value that indicates whether the pen input panel appears when focus is set on the attached control by using the pen. (IPenInputPanel.put_AutoShow)
helpviewer_keywords: ["AutoShow property [Tablet PC]","AutoShow property [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","AutoShow property","IPenInputPanel.AutoShow","IPenInputPanel.put_AutoShow","IPenInputPanel::AutoShow","IPenInputPanel::get_AutoShow","IPenInputPanel::put_AutoShow","PenInputPanel.get_AutoShow","PenInputPanel.put_AutoShow","c76533af-9b1d-413b-afa8-972ccfdce329","get_AutoShow","peninputpanel/IPenInputPanel::AutoShow","peninputpanel/IPenInputPanel::get_AutoShow","peninputpanel/IPenInputPanel::put_AutoShow","put_AutoShow","tablet.peninputpanel_autoshow"]
old-location: tablet\peninputpanel_autoshow.htm
tech.root: tablet
ms.assetid: c76533af-9b1d-413b-afa8-972ccfdce329
ms.date: 12/05/2018
ms.keywords: AutoShow property [Tablet PC], AutoShow property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],AutoShow property, IPenInputPanel.AutoShow, IPenInputPanel.put_AutoShow, IPenInputPanel::AutoShow, IPenInputPanel::get_AutoShow, IPenInputPanel::put_AutoShow, PenInputPanel.get_AutoShow, PenInputPanel.put_AutoShow, c76533af-9b1d-413b-afa8-972ccfdce329, get_AutoShow, peninputpanel/IPenInputPanel::AutoShow, peninputpanel/IPenInputPanel::get_AutoShow, peninputpanel/IPenInputPanel::put_AutoShow, put_AutoShow, tablet.peninputpanel_autoshow
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
 - IPenInputPanel::put_AutoShow
 - peninputpanel/IPenInputPanel::put_AutoShow
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
 - IPenInputPanel.AutoShow
 - IPenInputPanel.get_AutoShow
 - IPenInputPanel.put_AutoShow
 - PenInputPanel.get_AutoShow
 - PenInputPanel.put_AutoShow
---

# IPenInputPanel::put_AutoShow


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets or sets a value that indicates whether the pen input panel appears when focus is set on the attached control by using the pen.



This property is read/write.

## -parameters

## -remarks

When the <b>AutoShow</b> property is set to <b>VARIANT_FALSE</b>, Tablet PC Input Panel does not show until the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible">Visible</a> property is set to <b>VARIANT_TRUE</b>. At this point, Tablet PC Input Panel is displayed but no hover target is shown.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
