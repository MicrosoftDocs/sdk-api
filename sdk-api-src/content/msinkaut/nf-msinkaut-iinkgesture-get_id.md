---
UID: NF:msinkaut.IInkGesture.get_Id
title: IInkGesture::get_Id (msinkaut.h)
description: Gets the identifier of an object. (IInkGesture.get_Id)
helpviewer_keywords: ["ID property [Tablet PC]","ID property [Tablet PC]","IInkGesture interface","IInkGesture interface [Tablet PC]","ID property","IInkGesture.ID","IInkGesture.get_Id","IInkGesture::ID","IInkGesture::get_ID","IInkGesture::get_Id","get_Id","msinkaut/IInkGesture::ID","msinkaut/IInkGesture::get_ID","tablet.iinkgesture_id"]
old-location: tablet\iinkgesture_id.htm
tech.root: tablet
ms.assetid: 9ed0fcb7-57f9-43f4-95d9-dd75e9e7bd3f
ms.date: 12/05/2018
ms.keywords: ID property [Tablet PC], ID property [Tablet PC],IInkGesture interface, IInkGesture interface [Tablet PC],ID property, IInkGesture.ID, IInkGesture.get_Id, IInkGesture::ID, IInkGesture::get_ID, IInkGesture::get_Id, get_Id, msinkaut/IInkGesture::ID, msinkaut/IInkGesture::get_ID, tablet.iinkgesture_id
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
 - IInkGesture::get_Id
 - msinkaut/IInkGesture::get_Id
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
 - IInkGesture.ID
 - IInkGesture.get_ID
 - IInkGesture.get_Id
---

# IInkGesture::get_Id


## -description

Gets the identifier of an object.



This property is read-only.

## -parameters

## -remarks

An object's identifier never changes.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>; <b>WM_ACTIVATEAPP</b>; <b>WM_NCACTIVATE</b>; <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to <b>SC_HOTKEY</b> or <b>SC_TASKLIST</b>; and <b>WM_SYSKEYDOWN</b> (when processing ALT+TAB or ALT+ESC key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture Interface</a>
