---
UID: NF:peninputpanel.IPenInputPanel.get_Height
title: IPenInputPanel::get_Height (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the height of the pen input panel in client coordinates.
helpviewer_keywords: ["5815f184-1ae4-4617-9aa6-acf727aff202","Height property [Tablet PC]","Height property [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","Height property","IPenInputPanel.Height","IPenInputPanel.get_Height","IPenInputPanel::Height","IPenInputPanel::get_Height","PenInputPanel.get_Height","get_Height","peninputpanel/IPenInputPanel::Height","peninputpanel/IPenInputPanel::get_Height","tablet.peninputpanel_height"]
old-location: tablet\peninputpanel_height.htm
tech.root: tablet
ms.assetid: 5815f184-1ae4-4617-9aa6-acf727aff202
ms.date: 12/05/2018
ms.keywords: 5815f184-1ae4-4617-9aa6-acf727aff202, Height property [Tablet PC], Height property [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],Height property, IPenInputPanel.Height, IPenInputPanel.get_Height, IPenInputPanel::Height, IPenInputPanel::get_Height, PenInputPanel.get_Height, get_Height, peninputpanel/IPenInputPanel::Height, peninputpanel/IPenInputPanel::get_Height, tablet.peninputpanel_height
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
 - IPenInputPanel::get_Height
 - peninputpanel/IPenInputPanel::get_Height
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
 - IPenInputPanel.Height
 - IPenInputPanel.get_Height
 - PenInputPanel.get_Height
---

# IPenInputPanel::get_Height


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

Gets the height of the pen input panel in client coordinates.



This property is read-only.

## -parameters

## -remarks

The height of the pen input panel is dependent on the screen resolution for the particular Tablet PC. The panel height is the number of pixels equal to 1.25 inches. The default value at 96 dots per inch (dpi) is 157 pixels. The default value at 120 dpi is 196 pixels. The default value at 133 dpi is 218 pixels.

Starting with Microsoft Windows XP Tablet PC Edition 2005, the Tablet PC Input Panel allows the user to continue entering handwriting by automatically increasing the size of the Tablet PC Input Panel to accommodate new handwriting. The <b>Height</b> and <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width">Width</a> properties do not update to reflect the new size as the Tablet PC Input Panel grows. These properties return the original size of the Tablet PC Input Panel. They also do not report the dimensions of the Tablet PC Input Panel hover target.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width">Width Property [PenInputPanel Class]</a>
