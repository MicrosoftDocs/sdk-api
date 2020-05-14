---
UID: NF:msinkaut.IInkOverlay.put_SupportHighContrastSelectionUI
title: IInkOverlay::put_SupportHighContrastSelectionUI (msinkaut.h)
description: Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.helpviewer_keywords: ["IInkOverlay","IInkOverlay interface [Tablet PC]","SupportHighContrastSelectionUI property","IInkOverlay.SupportHighContrastSelectionUI","IInkOverlay.put_SupportHighContrastSelectionUI","IInkOverlay::SupportHighContrastSelectionUI","IInkOverlay::get_SupportHighContrastSelectionUI","IInkOverlay::put_SupportHighContrastSelectionUI","InkOverlay.get_SupportHighContrastSelectionUI","InkOverlay.put_SupportHighContrastSelectionUI","SupportHighContrastSelectionUI property [Tablet PC]","SupportHighContrastSelectionUI property [Tablet PC]","IInkOverlay interface","a8837657-6eb0-44d3-8c39-11a5524fe9db","msinkaut/IInkOverlay::SupportHighContrastSelectionUI","msinkaut/IInkOverlay::get_SupportHighContrastSelectionUI","msinkaut/IInkOverlay::put_SupportHighContrastSelectionUI","put_SupportHighContrastSelectionUI","tablet.inkoverlay_supporthighcontrastselectionui"]
old-location: tablet\inkoverlay_supporthighcontrastselectionui.htm
tech.root: tablet
ms.assetid: a8837657-6eb0-44d3-8c39-11a5524fe9db
ms.date: 12/05/2018
ms.keywords: IInkOverlay, IInkOverlay interface [Tablet PC],SupportHighContrastSelectionUI property, IInkOverlay.SupportHighContrastSelectionUI, IInkOverlay.put_SupportHighContrastSelectionUI, IInkOverlay::SupportHighContrastSelectionUI, IInkOverlay::get_SupportHighContrastSelectionUI, IInkOverlay::put_SupportHighContrastSelectionUI, InkOverlay.get_SupportHighContrastSelectionUI, InkOverlay.put_SupportHighContrastSelectionUI, SupportHighContrastSelectionUI property [Tablet PC], SupportHighContrastSelectionUI property [Tablet PC],IInkOverlay interface, a8837657-6eb0-44d3-8c39-11a5524fe9db, msinkaut/IInkOverlay::SupportHighContrastSelectionUI, msinkaut/IInkOverlay::get_SupportHighContrastSelectionUI, msinkaut/IInkOverlay::put_SupportHighContrastSelectionUI, put_SupportHighContrastSelectionUI, tablet.inkoverlay_supporthighcontrastselectionui
f1_keywords:
- msinkaut/IInkOverlay.SupportHighContrastSelectionUI
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkOverlay.SupportHighContrastSelectionUI
- IInkOverlay.get_SupportHighContrastSelectionUI
- IInkOverlay.put_SupportHighContrastSelectionUI
- InkOverlay.get_SupportHighContrastSelectionUI
- InkOverlay.put_SupportHighContrastSelectionUI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkOverlay::put_SupportHighContrastSelectionUI


## -description



Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way selection UI is displayed when the system changes to High Contrast mode. Selection UI elements include the selection bounding box and the selection handles.

Ink selection uses the COLOR_WINDOWTEXT, COLOR_WINDOW, and COLOR_HIGHLIGHT system colors to draw elements of the selection UI when the system is in High Contrast mode and the <b>SupportHighContrastSelectionUI</b> property is <b>TRUE</b>. For more information on system colors, see the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function in MSDN.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink">SupportHighContrastInk Property</a>
 

 

