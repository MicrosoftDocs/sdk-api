---
UID: NF:msinkaut.IInkCollector.get_MousePointer
title: IInkCollector::get_MousePointer (msinkaut.h)
description: Gets or sets a value that indicates the type of mouse pointer that appears. (IInkCollector.get_MousePointer)
helpviewer_keywords: ["8876b0ef-1a61-481b-ac37-9e4d637f8097","IInkCollector interface [Tablet PC]","MousePointer property","IInkCollector.MousePointer","IInkCollector.get_MousePointer","IInkCollector.put_MousePointer","IInkCollector::MousePointer","IInkCollector::get_MousePointer","IInkCollector::put_MousePointer","InkCollector.get_MousePointer","InkCollector.put_MousePointer","MousePointer property [Tablet PC]","MousePointer property [Tablet PC]","IInkCollector interface","get_MousePointer","msinkaut/IInkCollector::MousePointer","msinkaut/IInkCollector::get_MousePointer","msinkaut/IInkCollector::put_MousePointer","put_MousePointer","tablet.inkcollector_mousepointer"]
old-location: tablet\inkcollector_mousepointer.htm
tech.root: tablet
ms.assetid: 8876b0ef-1a61-481b-ac37-9e4d637f8097
ms.date: 12/05/2018
ms.keywords: 8876b0ef-1a61-481b-ac37-9e4d637f8097, IInkCollector interface [Tablet PC],MousePointer property, IInkCollector.MousePointer, IInkCollector.get_MousePointer, IInkCollector.put_MousePointer, IInkCollector::MousePointer, IInkCollector::get_MousePointer, IInkCollector::put_MousePointer, InkCollector.get_MousePointer, InkCollector.put_MousePointer, MousePointer property [Tablet PC], MousePointer property [Tablet PC],IInkCollector interface, get_MousePointer, msinkaut/IInkCollector::MousePointer, msinkaut/IInkCollector::get_MousePointer, msinkaut/IInkCollector::put_MousePointer, put_MousePointer, tablet.inkcollector_mousepointer
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
 - IInkCollector::get_MousePointer
 - msinkaut/IInkCollector::get_MousePointer
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
 - IInkCollector.MousePointer
 - IInkCollector.get_MousePointer
 - IInkCollector.put_MousePointer
 - put_MousePointer
 - IInkCollector.put_MousePointer
 - InkCollector.get_MousePointer
 - InkCollector.put_MousePointer
---

# IInkCollector::get_MousePointer


## -description

Gets or sets a value that indicates the type of mouse pointer that appears.



This property is read/write.

## -parameters

## -remarks

If you set the <b>MousePointer</b> property to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Default</a>, the mouse cursor setting is based on the current cursor's drawing attributes. If the ink collector is disabled, the mouse cursor setting is based on the underlying windows mouse cursor <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes">DrawingAttributes</a> property. If the <b>MousePointer</b> property is set to <b>IMP_Custom</b> and the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon</a> property is <b>NULL</b>, then the ink collector no longer handles mouse cursor settings. Setting the mouse cursor to any other setting (other than the <b>MousePointer</b> property set to <b>IMP_Default</b> and the <b>MouseIcon</b> property set to <b>NULL</b>) forces the mouse cursor to use the current setting.

You can use this property when you want to indicate changes in functionality as the mouse pointer passes over controls on a form or dialog box. The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Hourglass</a> setting is useful for indicating that the user should wait for a process or operation to finish.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">InkMousePointer Enumeration</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon Property</a>
