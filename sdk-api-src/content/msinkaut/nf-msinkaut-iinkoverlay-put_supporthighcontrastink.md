---
UID: NF:msinkaut.IInkOverlay.put_SupportHighContrastInk
title: IInkOverlay::put_SupportHighContrastInk (msinkaut.h)
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. (IInkOverlay.put_SupportHighContrastInk)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","SupportHighContrastInk property","IInkOverlay.SupportHighContrastInk","IInkOverlay.put_SupportHighContrastInk","IInkOverlay::SupportHighContrastInk","IInkOverlay::get_SupportHighContrastInk","IInkOverlay::put_SupportHighContrastInk","InkOverlay.get_SupportHighContrastInk","InkOverlay.put_SupportHighContrastInk","SupportHighContrastInk property [Tablet PC]","SupportHighContrastInk property [Tablet PC]","IInkOverlay interface","get_SupportHighContrastInk","msinkaut/IInkOverlay::SupportHighContrastInk","msinkaut/IInkOverlay::get_SupportHighContrastInk","msinkaut/IInkOverlay::put_SupportHighContrastInk","put_SupportHighContrastInk","tablet.inkoverlay_supporthighcontrastink"]
old-location: tablet\inkoverlay_supporthighcontrastink.htm
tech.root: tablet
ms.assetid: 69c0c628-e377-4c26-8fb7-1f0574fbff29
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],SupportHighContrastInk property, IInkOverlay.SupportHighContrastInk, IInkOverlay.put_SupportHighContrastInk, IInkOverlay::SupportHighContrastInk, IInkOverlay::get_SupportHighContrastInk, IInkOverlay::put_SupportHighContrastInk, InkOverlay.get_SupportHighContrastInk, InkOverlay.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkOverlay interface, get_SupportHighContrastInk, msinkaut/IInkOverlay::SupportHighContrastInk, msinkaut/IInkOverlay::get_SupportHighContrastInk, msinkaut/IInkOverlay::put_SupportHighContrastInk, put_SupportHighContrastInk, tablet.inkoverlay_supporthighcontrastink
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
 - IInkOverlay::put_SupportHighContrastInk
 - msinkaut/IInkOverlay::put_SupportHighContrastInk
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
 - IInkOverlay.SupportHighContrastInk
 - IInkOverlay.get_SupportHighContrastInk
 - IInkOverlay.put_SupportHighContrastInk
 - InkOverlay.get_SupportHighContrastInk
 - InkOverlay.put_SupportHighContrastInk
---

# IInkOverlay::put_SupportHighContrastInk


## -description

Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.

## -parameters

## -remarks

This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink">SupportHighContrastInk</a> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color</a> property is set to <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes">DefaultDrawingAttributes Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui">SupportHighContrastSelectionUI Property [InkOverlay Class]</a>
