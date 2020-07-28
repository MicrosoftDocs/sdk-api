---
UID: NF:msinkaut.IInkOverlay.get_MousePointer
title: IInkOverlay::get_MousePointer (msinkaut.h)
description: Gets or sets a value that indicates the type of mouse pointer that appears.
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","MousePointer property","IInkOverlay.MousePointer","IInkOverlay.get_MousePointer","IInkOverlay::MousePointer","IInkOverlay::get_MousePointer","IInkOverlay::put_MousePointer","InkOverlay.get_MousePointer","InkOverlay.put_MousePointer","MousePointer property [Tablet PC]","MousePointer property [Tablet PC]","IInkOverlay interface","get_MousePointer","msinkaut/IInkOverlay::MousePointer","msinkaut/IInkOverlay::get_MousePointer","msinkaut/IInkOverlay::put_MousePointer","put_MousePointer","tablet.inkoverlay_mousepointer"]
old-location: tablet\inkoverlay_mousepointer.htm
tech.root: tablet
ms.assetid: cf687894-b005-4a86-9a71-dc27b225b1e4
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],MousePointer property, IInkOverlay.MousePointer, IInkOverlay.get_MousePointer, IInkOverlay::MousePointer, IInkOverlay::get_MousePointer, IInkOverlay::put_MousePointer, InkOverlay.get_MousePointer, InkOverlay.put_MousePointer, MousePointer property [Tablet PC], MousePointer property [Tablet PC],IInkOverlay interface, get_MousePointer, msinkaut/IInkOverlay::MousePointer, msinkaut/IInkOverlay::get_MousePointer, msinkaut/IInkOverlay::put_MousePointer, put_MousePointer, tablet.inkoverlay_mousepointer
f1_keywords:
- msinkaut/IInkOverlay.MousePointer
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
- IInkOverlay.MousePointer
- IInkOverlay.get_MousePointer
- IInkOverlay.put_MousePointer
- InkOverlay.get_MousePointer
- InkOverlay.put_MousePointer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkOverlay::get_MousePointer


## -description



Gets or sets a value that indicates the type of mouse pointer that appears.



This property is read/write.


## -parameters


## -remarks



If you set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer</a> property to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Default</a>, the mouse cursor setting is based on the current cursor's drawing attributes. If the ink collector is disabled, the mouse cursor setting is based on the underlying windows mouse cursor <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property. If the <b>MousePointer</b> property is set to <b>IMP_Custom</b> and the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon</a> property is <b>NULL</b>, then the ink collector no longer handles mouse cursor settings. Setting the mouse cursor to any other setting (other than the <b>MousePointer</b> property set to <b>IMP_Default</b> and the <b>MouseIcon</b> property set to <b>NULL</b>) forces the mouse cursor to use the current setting.

You can use this property when you want to indicate changes in functionality as the mouse pointer passes over controls on a form or dialog box. The <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Hourglass</a> setting is useful for indicating that the user should wait for a process or operation to finish.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">InkMousePointer Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon Property</a>
 

 

