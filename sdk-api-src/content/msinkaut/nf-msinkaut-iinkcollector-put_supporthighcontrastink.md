---
UID: NF:msinkaut.IInkCollector.put_SupportHighContrastInk
title: IInkCollector::put_SupportHighContrastInk (msinkaut.h)
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. (IInkCollector.put_SupportHighContrastInk)
helpviewer_keywords: ["17f5002b-0191-4cb0-8b12-0383aaabe2a8","IInkCollector interface [Tablet PC]","SupportHighContrastInk property","IInkCollector.SupportHighContrastInk","IInkCollector.put_SupportHighContrastInk","IInkCollector::SupportHighContrastInk","IInkCollector::get_SupportHighContrastInk","IInkCollector::put_SupportHighContrastInk","InkCollector.get_SupportHighContrastInk","InkCollector.put_SupportHighContrastInk","SupportHighContrastInk property [Tablet PC]","SupportHighContrastInk property [Tablet PC]","IInkCollector interface","get_SupportHighContrastInk","msinkaut/IInkCollector::SupportHighContrastInk","msinkaut/IInkCollector::get_SupportHighContrastInk","msinkaut/IInkCollector::put_SupportHighContrastInk","put_SupportHighContrastInk","tablet.inkcollector_supporthighcontrastink"]
old-location: tablet\inkcollector_supporthighcontrastink.htm
tech.root: tablet
ms.assetid: 17f5002b-0191-4cb0-8b12-0383aaabe2a8
ms.date: 12/05/2018
ms.keywords: 17f5002b-0191-4cb0-8b12-0383aaabe2a8, IInkCollector interface [Tablet PC],SupportHighContrastInk property, IInkCollector.SupportHighContrastInk, IInkCollector.put_SupportHighContrastInk, IInkCollector::SupportHighContrastInk, IInkCollector::get_SupportHighContrastInk, IInkCollector::put_SupportHighContrastInk, InkCollector.get_SupportHighContrastInk, InkCollector.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkCollector interface, get_SupportHighContrastInk, msinkaut/IInkCollector::SupportHighContrastInk, msinkaut/IInkCollector::get_SupportHighContrastInk, msinkaut/IInkCollector::put_SupportHighContrastInk, put_SupportHighContrastInk, tablet.inkcollector_supporthighcontrastink
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
 - IInkCollector::put_SupportHighContrastInk
 - msinkaut/IInkCollector::put_SupportHighContrastInk
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
 - IInkCollector.SupportHighContrastInk
 - IInkCollector.get_SupportHighContrastInk
 - IInkCollector.put_SupportHighContrastInk
 - InkCollector.get_SupportHighContrastInk
 - InkCollector.put_SupportHighContrastInk
---

# IInkCollector::put_SupportHighContrastInk


## -description

Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.

## -parameters

## -remarks

This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <b>SupportHighContrastInk</b> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color</a> property is set to <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes Property</a>



<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui">SupportHighContrastSelectionUI Property [InkOverlay Class]</a>
