---
UID: NF:inked.IInkEdit.get_InkMode
title: IInkEdit::get_InkMode (inked.h)
description: Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected. (Get)
helpviewer_keywords: ["0e395907-108b-40cf-819b-65a34e4ffc4d","Disabled","IInkEdit interface [Tablet PC]","InkMode property","IInkEdit.InkMode","IInkEdit.get_InkMode","IInkEdit::InkMode","IInkEdit::get_InkMode","IInkEdit::put_InkMode","Ink","InkAndGesture","InkEdit.get_InkMode","InkEdit.put_InkMode","InkMode property [Tablet PC]","InkMode property [Tablet PC]","IInkEdit interface","get_InkMode","inked/IInkEdit::InkMode","inked/IInkEdit::get_InkMode","inked/IInkEdit::put_InkMode","put_InkMode","tablet.inkedit_inkmode"]
old-location: tablet\inkedit_inkmode.htm
tech.root: tablet
ms.assetid: 0e395907-108b-40cf-819b-65a34e4ffc4d
ms.date: 12/05/2018
ms.keywords: 0e395907-108b-40cf-819b-65a34e4ffc4d, Disabled, IInkEdit interface [Tablet PC],InkMode property, IInkEdit.InkMode, IInkEdit.get_InkMode, IInkEdit::InkMode, IInkEdit::get_InkMode, IInkEdit::put_InkMode, Ink, InkAndGesture, InkEdit.get_InkMode, InkEdit.put_InkMode, InkMode property [Tablet PC], InkMode property [Tablet PC],IInkEdit interface, get_InkMode, inked/IInkEdit::InkMode, inked/IInkEdit::get_InkMode, inked/IInkEdit::put_InkMode, put_InkMode, tablet.inkedit_inkmode
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
 - IInkEdit::get_InkMode
 - inked/IInkEdit::get_InkMode
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
 - IInkEdit.InkMode
 - IInkEdit.get_InkMode
 - IInkEdit.put_InkMode
 - InkEdit.get_InkMode
 - InkEdit.put_InkMode
---

# IInkEdit::get_InkMode


## -description

Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected.



This property is read/write.

## -parameters

## -remarks

The value of this property is always Disabled if it is used on a system that has Microsoft Windows XP Tablet PC Edition installed but no recognizers are present. If used on a system with Windows Vista or Windows XP Tablet PC Edition installed, the value can be set to any of the values in the <a href="/windows/desktop/api/inked/ne-inked-inkmode">InkMode</a> enumeration type.

This property should be changed only if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns IES_Idle.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/api/inked/ne-inked-inkmode">InkMode Enumeration</a>
