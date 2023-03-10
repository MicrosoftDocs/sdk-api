---
UID: NF:msinkaut.IInkCursor.get_Tablet
title: IInkCursor::get_Tablet (msinkaut.h)
description: Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. (IInkCursor.get_Tablet)
helpviewer_keywords: ["85bbf314-e1fe-43fb-b743-d648aa6a54cd","IInkCursor interface [Tablet PC]","Tablet property","IInkCursor.Tablet","IInkCursor.get_Tablet","IInkCursor::Tablet","IInkCursor::get_Tablet","Tablet property [Tablet PC]","Tablet property [Tablet PC]","IInkCursor interface","get_Tablet","msinkaut/IInkCursor::Tablet","msinkaut/IInkCursor::get_Tablet","tablet.inkcursor_tablet"]
old-location: tablet\inkcursor_tablet.htm
tech.root: tablet
ms.assetid: 85bbf314-e1fe-43fb-b743-d648aa6a54cd
ms.date: 12/05/2018
ms.keywords: 85bbf314-e1fe-43fb-b743-d648aa6a54cd, IInkCursor interface [Tablet PC],Tablet property, IInkCursor.Tablet, IInkCursor.get_Tablet, IInkCursor::Tablet, IInkCursor::get_Tablet, Tablet property [Tablet PC], Tablet property [Tablet PC],IInkCursor interface, get_Tablet, msinkaut/IInkCursor::Tablet, msinkaut/IInkCursor::get_Tablet, tablet.inkcursor_tablet
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
 - IInkCursor::get_Tablet
 - msinkaut/IInkCursor::get_Tablet
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
 - IInkCursor.Tablet
 - IInkCursor.get_Tablet
 - IInkCursor.get_Tablet
---

# IInkCursor::get_Tablet


## -description

Gets either the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object to which a cursor belongs or the <b>IInkTablet</b> object that an object or control is currently using to collect input.



This property is read-only.

## -parameters

## -remarks

For an object or control that collects ink, this property is valid only when the object or control is collecting ink from just one tablet. Accessing this property for an object or control that is collecting ink from all tablets generates an exception.

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursorbutton-get_id">Id Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">InkCursor Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>
