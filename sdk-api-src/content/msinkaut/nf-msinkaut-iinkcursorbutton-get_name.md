---
UID: NF:msinkaut.IInkCursorButton.get_Name
title: IInkCursorButton::get_Name (msinkaut.h)
description: Gets the name of the object. (IInkCursorButton.get_Name)
helpviewer_keywords: ["IInkCursorButton interface [Tablet PC]","Name property","IInkCursorButton.Name","IInkCursorButton.get_Name","IInkCursorButton::Name","IInkCursorButton::get_Name","Name property [Tablet PC]","Name property [Tablet PC]","IInkCursorButton interface","get_Name","msinkaut/IInkCursorButton::Name","msinkaut/IInkCursorButton::get_Name","tablet.iinkcursorbutton_name"]
old-location: tablet\iinkcursorbutton_name.htm
tech.root: tablet
ms.assetid: a431a359-12ea-4ac2-a966-6ad45a63e646
ms.date: 12/05/2018
ms.keywords: IInkCursorButton interface [Tablet PC],Name property, IInkCursorButton.Name, IInkCursorButton.get_Name, IInkCursorButton::Name, IInkCursorButton::get_Name, Name property [Tablet PC], Name property [Tablet PC],IInkCursorButton interface, get_Name, msinkaut/IInkCursorButton::Name, msinkaut/IInkCursorButton::get_Name, tablet.iinkcursorbutton_name
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
 - IInkCursorButton::get_Name
 - msinkaut/IInkCursorButton::get_Name
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
 - IInkCursorButton.Name
 - IInkCursorButton.get_Name
 - IInkCursorButton.get_Name
---

# IInkCursorButton::get_Name


## -description

Gets the name of the object.



This property is read-only.

## -parameters

## -remarks

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, WM_PAINT; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a>
