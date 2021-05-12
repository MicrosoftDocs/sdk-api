---
UID: NF:peninputpanel.IPenInputPanel.get_Width
title: IPenInputPanel::get_Width (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the width of the pen input panel in client coordinates.
helpviewer_keywords: ["81173c64-5d8b-48ae-866c-5292814a97c0","IPenInputPanel interface [Tablet PC]","Width property","IPenInputPanel.Width","IPenInputPanel.get_Width","IPenInputPanel::Width","IPenInputPanel::get_Width","PenInputPanel.get_Width","Width property [Tablet PC]","Width property [Tablet PC]","IPenInputPanel interface","get_Width","peninputpanel/IPenInputPanel::Width","peninputpanel/IPenInputPanel::get_Width","put_Width","tablet.peninputpanel_width"]
old-location: tablet\peninputpanel_width.htm
tech.root: tablet
ms.assetid: 81173c64-5d8b-48ae-866c-5292814a97c0
ms.date: 12/05/2018
ms.keywords: 81173c64-5d8b-48ae-866c-5292814a97c0, IPenInputPanel interface [Tablet PC],Width property, IPenInputPanel.Width, IPenInputPanel.get_Width, IPenInputPanel::Width, IPenInputPanel::get_Width, PenInputPanel.get_Width, Width property [Tablet PC], Width property [Tablet PC],IPenInputPanel interface, get_Width, peninputpanel/IPenInputPanel::Width, peninputpanel/IPenInputPanel::get_Width, put_Width, tablet.peninputpanel_width
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
 - IPenInputPanel::get_Width
 - peninputpanel/IPenInputPanel::get_Width
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
 - IPenInputPanel.Width
 - IPenInputPanel.get_Width
 - PenInputPanel.get_Width
---

# IPenInputPanel::get_Width


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the width of the pen input panel  in client coordinates.



This property is read-only.

## -parameters

## -remarks

The width of the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is dependent on the screen resolution for the particular Tablet PC. The default value at 96 dots per inch (dpi) is 570 pixels. The default value at 120 dpi is 712 pixels. The default value at 133 dpi is 790 pixels.

Starting with Microsoft Windows XP Tablet PC Edition 2005, the Tablet PC Input Panel allows the user to continue entering handwriting by automatically increasing the size of the Tablet PC Input Panel to accommodate new handwriting. The <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height">Height</a> and <b>Width</b> properties do not update to reflect the new size as the Tablet PC Input Panel grows. These properties return the original size of the Tablet PC Input Panel. They also do not report the dimensions of the Tablet PC Input Panel hover target.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height">Height Property [PenInputPanel Class]</a>



<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
