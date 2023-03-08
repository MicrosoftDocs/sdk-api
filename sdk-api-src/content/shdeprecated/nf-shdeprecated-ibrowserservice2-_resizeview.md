---
UID: NF:shdeprecated.IBrowserService2._ResizeView
title: IBrowserService2::_ResizeView (shdeprecated.h)
description: Deprecated. Calls IBrowserService2::_UpdateViewRectSize, then updates the browser view by using IOleInPlaceActiveObject::ResizeBorder.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_ResizeView method","IBrowserService2._ResizeView","IBrowserService2::_ResizeView","_ResizeView","_ResizeView method [Windows Shell]","_ResizeView method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_ResizeView","shell.IBrowserService2__ResizeView","zone_IBrowserService2__ResizeView"]
old-location: shell\IBrowserService2__ResizeView.htm
tech.root: shell
ms.assetid: 12b38906-f22a-490d-9b2f-192eb43a8305
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_ResizeView method, IBrowserService2._ResizeView, IBrowserService2::_ResizeView, _ResizeView, _ResizeView method [Windows Shell], _ResizeView method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_ResizeView, shell.IBrowserService2__ResizeView, zone_IBrowserService2__ResizeView
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::_ResizeView
 - shdeprecated/IBrowserService2::_ResizeView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2._ResizeView
---

# IBrowserService2::_ResizeView


## -description

Deprecated. Calls <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_updateviewrectsize">IBrowserService2::_UpdateViewRectSize</a>, then updates the browser view by using <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceactiveobject-resizeborder">IOleInPlaceActiveObject::ResizeBorder</a>.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
