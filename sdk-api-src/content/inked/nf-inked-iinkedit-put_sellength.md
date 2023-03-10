---
UID: NF:inked.IInkEdit.put_SelLength
title: IInkEdit::put_SelLength (inked.h)
description: Gets or sets the number of characters that are selected in the InkEdit control (run time only). (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelLength property","IInkEdit.SelLength","IInkEdit.put_SelLength","IInkEdit::SelLength","IInkEdit::get_SelLength","IInkEdit::put_SelLength","InkEdit.get_SelLength","InkEdit.put_SelLength","SelLength property [Tablet PC]","SelLength property [Tablet PC]","IInkEdit interface","get_SelLength","inked/IInkEdit::SelLength","inked/IInkEdit::get_SelLength","inked/IInkEdit::put_SelLength","put_SelLength","tablet.inkedit_sellength"]
old-location: tablet\inkedit_sellength.htm
tech.root: tablet
ms.assetid: 6295a536-831e-4603-9412-87b2fa5b7f53
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelLength property, IInkEdit.SelLength, IInkEdit.put_SelLength, IInkEdit::SelLength, IInkEdit::get_SelLength, IInkEdit::put_SelLength, InkEdit.get_SelLength, InkEdit.put_SelLength, SelLength property [Tablet PC], SelLength property [Tablet PC],IInkEdit interface, get_SelLength, inked/IInkEdit::SelLength, inked/IInkEdit::get_SelLength, inked/IInkEdit::put_SelLength, put_SelLength, tablet.inkedit_sellength
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
 - IInkEdit::put_SelLength
 - inked/IInkEdit::put_SelLength
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
 - IInkEdit.SelLength
 - IInkEdit.get_SelLength
 - IInkEdit.put_SelLength
 - InkEdit.get_SelLength
 - InkEdit.put_SelLength
---

# IInkEdit::put_SelLength


## -description

Gets or sets the number of characters that are selected in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

This property is read/write.

## -parameters

## -remarks

You can use this property to determine if any characters are currently selected in the text box control before performing operations on the selected text. You can also use this property to determine the total number of characters (including spaces) that are selected when performing single character tasks in a for loop.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
