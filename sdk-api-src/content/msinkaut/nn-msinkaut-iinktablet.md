---
UID: NN:msinkaut.IInkTablet
title: IInkTablet (msinkaut.h)
description: Represents the digitizer device of Tablet PC that receives tablet device messages or events.
helpviewer_keywords: ["9a945740-b191-41f5-8b3d-49b7e2d1e463","IInkTablet","IInkTablet interface [Tablet PC]","IInkTablet interface [Tablet PC]","described","msinkaut/IInkTablet","tablet.iinktablet"]
old-location: tablet\iinktablet.htm
tech.root: tablet
ms.assetid: 9a945740-b191-41f5-8b3d-49b7e2d1e463
ms.date: 12/05/2018
ms.keywords: 9a945740-b191-41f5-8b3d-49b7e2d1e463, IInkTablet, IInkTablet interface [Tablet PC], IInkTablet interface [Tablet PC],described, msinkaut/IInkTablet, tablet.iinktablet
req.header: msinkaut.h
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
 - IInkTablet
 - msinkaut/IInkTablet
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
 - IInkTablet
---

# IInkTablet interface


## -description

Represents the digitizer device of Tablet PC that receives tablet device messages or events.

## -inheritance

The <b>IInkTablet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkTablet</b> also has these types of members:

## -remarks

You can use the <b>IInkTablet</b> object to determine the hardware capabilities of the tablet device. A Tablet PC may have more than one digitizer attached in addition to the built-in digitizer.

<b>IInkTablet</b> objects work closely with ink collector objects. An ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) can be set to one of two tablet-related modes:

<ul>
<li>All tablets mode</li>
<li>Single tablet integrated mode</li>
</ul>
The default mode is all tablets mode (set with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a> method of the ink collector). This mode integrates all tablet devices if multiple devices are attached to the Tablet PC. Because all of the tablets are integrated, available cursors can be used on any of the tablet devices, and each tablet maps to the entire screen. This allows automatic updating of the windows.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>
