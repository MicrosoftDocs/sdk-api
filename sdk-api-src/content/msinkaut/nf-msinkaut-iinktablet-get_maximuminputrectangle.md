---
UID: NF:msinkaut.IInkTablet.get_MaximumInputRectangle
title: IInkTablet::get_MaximumInputRectangle (msinkaut.h)
description: Gets the maximum input rectangle, in tablet device coordinates that the IInkTablet object supports.
helpviewer_keywords: ["84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43","IInkTablet interface [Tablet PC]","MaximumInputRectangle property","IInkTablet.MaximumInputRectangle","IInkTablet.get_MaximumInputRectangle","IInkTablet::MaximumInputRectangle","IInkTablet::get_MaximumInputRectangle","MaximumInputRectangle property [Tablet PC]","MaximumInputRectangle property [Tablet PC]","IInkTablet interface","get_MaximumInputRectangle","msinkaut/IInkTablet::MaximumInputRectangle","msinkaut/IInkTablet::get_MaximumInputRectangle","tablet.iinktablet_maximuminputrectangle"]
old-location: tablet\iinktablet_maximuminputrectangle.htm
tech.root: tablet
ms.assetid: 84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43
ms.date: 12/05/2018
ms.keywords: 84d8518b-6cd7-4da9-9ce3-1ce6fe6eeb43, IInkTablet interface [Tablet PC],MaximumInputRectangle property, IInkTablet.MaximumInputRectangle, IInkTablet.get_MaximumInputRectangle, IInkTablet::MaximumInputRectangle, IInkTablet::get_MaximumInputRectangle, MaximumInputRectangle property [Tablet PC], MaximumInputRectangle property [Tablet PC],IInkTablet interface, get_MaximumInputRectangle, msinkaut/IInkTablet::MaximumInputRectangle, msinkaut/IInkTablet::get_MaximumInputRectangle, tablet.iinktablet_maximuminputrectangle
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
 - IInkTablet::get_MaximumInputRectangle
 - msinkaut/IInkTablet::get_MaximumInputRectangle
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
 - IInkTablet.MaximumInputRectangle
 - IInkTablet.get_MaximumInputRectangle
 - IInkTablet.get_MaximumInputRectangle
---

# IInkTablet::get_MaximumInputRectangle


## -description

Gets the maximum input rectangle, in tablet device coordinates that the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object supports.



This property is read-only.

## -parameters

## -remarks

The rectangle returned by the <b>MaximumInputRectangle</b> property specifies the maximum allowable space in which ink can be drawn.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>