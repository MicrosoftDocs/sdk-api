---
UID: NF:inked.IInkEdit.get_MousePointer
title: IInkEdit::get_MousePointer (inked.h)
description: Gets or sets a value indicating the type of mouse pointer to be displayed. (Get)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","MousePointer property","IInkEdit.MousePointer","IInkEdit.get_MousePointer","IInkEdit::MousePointer","IInkEdit::get_MousePointer","IInkEdit::put_MousePointer","InkEdit.get_MousePointer","InkEdit.put_MousePointer","MousePointer property [Tablet PC]","MousePointer property [Tablet PC]","IInkEdit interface","get_MousePointer","inked/IInkEdit::MousePointer","inked/IInkEdit::get_MousePointer","inked/IInkEdit::put_MousePointer","put_MousePointer","tablet.inkedit_mousepointer"]
old-location: tablet\inkedit_mousepointer.htm
tech.root: tablet
ms.assetid: a5d9a6cc-d777-4619-b28b-17cc79584171
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],MousePointer property, IInkEdit.MousePointer, IInkEdit.get_MousePointer, IInkEdit::MousePointer, IInkEdit::get_MousePointer, IInkEdit::put_MousePointer, InkEdit.get_MousePointer, InkEdit.put_MousePointer, MousePointer property [Tablet PC], MousePointer property [Tablet PC],IInkEdit interface, get_MousePointer, inked/IInkEdit::MousePointer, inked/IInkEdit::get_MousePointer, inked/IInkEdit::put_MousePointer, put_MousePointer, tablet.inkedit_mousepointer
req.header: inked.h
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
req.lib: InkEd.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkEdit::get_MousePointer
 - inked/IInkEdit::get_MousePointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.MousePointer
 - IInkEdit.get_MousePointer
 - IInkEdit.put_MousePointer
 - InkEdit.get_MousePointer
 - InkEdit.put_MousePointer
---

# IInkEdit::get_MousePointer


## -description

Gets or sets a value indicating the type of mouse pointer to be displayed.

This property is read/write.

## -parameters

## -remarks

If you set the <b>MousePointer</b> property to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Default</a>, the mouse cursor setting is based on the current cursor's drawing attributes. If the ink collector is disabled, the mouse cursor setting is based on the underlying windows mouse cursor <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes">DrawingAttributes</a> property. If the <b>MousePointer</b> property is set to <b>IMP_Custom</b> and the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon">MouseIcon</a> property is <b>NULL</b>, then the ink collector no longer handles mouse cursor settings. Setting the mouse cursor to any other setting (other than the <b>MousePointer</b> property set to <b>IMP_Default</b> and the <b>MouseIcon</b> property set to <b>NULL</b>) forces the mouse cursor to use the current setting.

You can use this property when you want to indicate changes in functionality as the mouse pointer passes over controls on a form or dialog box. The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Hourglass</a> setting is useful for indicating that the user should wait for a process or operation to finish.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
