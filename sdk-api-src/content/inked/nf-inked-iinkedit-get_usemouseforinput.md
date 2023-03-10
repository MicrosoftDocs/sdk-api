---
UID: NF:inked.IInkEdit.get_UseMouseForInput
title: IInkEdit::get_UseMouseForInput (inked.h)
description: Gets or sets a value that indicates whether the mouse can be used as an input device. (Get)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","UseMouseForInput property","IInkEdit.UseMouseForInput","IInkEdit.get_UseMouseForInput","IInkEdit::UseMouseForInput","IInkEdit::get_UseMouseForInput","IInkEdit::put_UseMouseForInput","InkEdit.get_UseMouseForInput","InkEdit.put_UseMouseForInput","UseMouseForInput property [Tablet PC]","UseMouseForInput property [Tablet PC]","IInkEdit interface","e4a425db-6a81-494d-818f-50a53d8c124b","get_UseMouseForInput","inked/IInkEdit::UseMouseForInput","inked/IInkEdit::get_UseMouseForInput","inked/IInkEdit::put_UseMouseForInput","put_UseMouseForInput","tablet.inkedit_usemouseforinput"]
old-location: tablet\inkedit_usemouseforinput.htm
tech.root: tablet
ms.assetid: e4a425db-6a81-494d-818f-50a53d8c124b
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],UseMouseForInput property, IInkEdit.UseMouseForInput, IInkEdit.get_UseMouseForInput, IInkEdit::UseMouseForInput, IInkEdit::get_UseMouseForInput, IInkEdit::put_UseMouseForInput, InkEdit.get_UseMouseForInput, InkEdit.put_UseMouseForInput, UseMouseForInput property [Tablet PC], UseMouseForInput property [Tablet PC],IInkEdit interface, e4a425db-6a81-494d-818f-50a53d8c124b, get_UseMouseForInput, inked/IInkEdit::UseMouseForInput, inked/IInkEdit::get_UseMouseForInput, inked/IInkEdit::put_UseMouseForInput, put_UseMouseForInput, tablet.inkedit_usemouseforinput
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
 - IInkEdit::get_UseMouseForInput
 - inked/IInkEdit::get_UseMouseForInput
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
 - IInkEdit.UseMouseForInput
 - IInkEdit.get_UseMouseForInput
 - IInkEdit.put_UseMouseForInput
 - InkEdit.get_UseMouseForInput
 - InkEdit.put_UseMouseForInput
---

# IInkEdit::get_UseMouseForInput


## -description

Gets or sets a value that indicates whether the mouse can be used as an input device.



This property is read/write.

## -parameters

## -remarks

This property should only be changed if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns IES_Idle.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
