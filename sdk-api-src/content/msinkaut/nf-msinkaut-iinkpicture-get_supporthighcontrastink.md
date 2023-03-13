---
UID: NF:msinkaut.IInkPicture.get_SupportHighContrastInk
title: IInkPicture::get_SupportHighContrastInk (msinkaut.h)
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. (IInkPicture.get_SupportHighContrastInk)
helpviewer_keywords: ["IInkPicture interface [Tablet PC]","SupportHighContrastInk property","IInkPicture.SupportHighContrastInk","IInkPicture.get_SupportHighContrastInk","IInkPicture::SupportHighContrastInk","IInkPicture::get_SupportHighContrastInk","IInkPicture::put_SupportHighContrastInk","InkPicture.get_SupportHighContrastInk","InkPicture.put_SupportHighContrastInk","SupportHighContrastInk property [Tablet PC]","SupportHighContrastInk property [Tablet PC]","IInkPicture interface","get_SupportHighContrastInk","msinkaut/IInkPicture::SupportHighContrastInk","msinkaut/IInkPicture::get_SupportHighContrastInk","msinkaut/IInkPicture::put_SupportHighContrastInk","putt_SupportHighContrastInk","tablet.inkpicture_supporthighcontrastink"]
old-location: tablet\inkpicture_supporthighcontrastink.htm
tech.root: tablet
ms.assetid: 9f57e1fe-8224-43ef-bd26-2d15da625725
ms.date: 12/05/2018
ms.keywords: IInkPicture interface [Tablet PC],SupportHighContrastInk property, IInkPicture.SupportHighContrastInk, IInkPicture.get_SupportHighContrastInk, IInkPicture::SupportHighContrastInk, IInkPicture::get_SupportHighContrastInk, IInkPicture::put_SupportHighContrastInk, InkPicture.get_SupportHighContrastInk, InkPicture.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkPicture interface, get_SupportHighContrastInk, msinkaut/IInkPicture::SupportHighContrastInk, msinkaut/IInkPicture::get_SupportHighContrastInk, msinkaut/IInkPicture::put_SupportHighContrastInk, putt_SupportHighContrastInk, tablet.inkpicture_supporthighcontrastink
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
 - IInkPicture::get_SupportHighContrastInk
 - msinkaut/IInkPicture::get_SupportHighContrastInk
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
 - IInkPicture.SupportHighContrastInk
 - IInkPicture.get_SupportHighContrastInk
 - IInkPicture.put_SupportHighContrastInk
 - InkPicture.get_SupportHighContrastInk
 - InkPicture.put_SupportHighContrastInk
---

# IInkPicture::get_SupportHighContrastInk


## -description

Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.

## -parameters

## -remarks

This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <b>SupportHighContrastInk</b> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color</a> property is set to <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes">DefaultDrawingAttributes Property</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui">SupportHighContrastSelectionUI Property [InkPicture Control]</a>
