---
UID: NF:msinkaut.IInkTablet.get_Name
title: IInkTablet::get_Name (msinkaut.h)
description: Gets the name of the object. (IInkTablet.get_Name)
helpviewer_keywords: ["IInkTablet interface [Tablet PC]","Name property","IInkTablet.Name","IInkTablet.get_Name","IInkTablet::Name","IInkTablet::get_Name","Name property [Tablet PC]","Name property [Tablet PC]","IInkTablet interface","get_Name","msinkaut/IInkTablet::Name","msinkaut/IInkTablet::get_Name","tablet.iinktablet_name"]
old-location: tablet\iinktablet_name.htm
tech.root: tablet
ms.assetid: 8388ca02-b464-47e4-9911-1c55ce398557
ms.date: 12/05/2018
ms.keywords: IInkTablet interface [Tablet PC],Name property, IInkTablet.Name, IInkTablet.get_Name, IInkTablet::Name, IInkTablet::get_Name, Name property [Tablet PC], Name property [Tablet PC],IInkTablet interface, get_Name, msinkaut/IInkTablet::Name, msinkaut/IInkTablet::get_Name, tablet.iinktablet_name
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
 - IInkTablet::get_Name
 - msinkaut/IInkTablet::get_Name
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
 - IInkTablet.Name
 - IInkTablet.get_Name
 - IInkTablet.get_Name
---

# IInkTablet::get_Name


## -description

Gets the name of the object.



This property is read-only.

## -parameters

## -remarks

Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, WM_PAINT; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>
