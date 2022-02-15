---
UID: NF:shdeprecated.IBrowserService2.CreateViewWindow
title: IBrowserService2::CreateViewWindow (shdeprecated.h)
description: Deprecated. Coordinates the updating of state when creating a new browser view window.
helpviewer_keywords: ["CreateViewWindow","CreateViewWindow method [Windows Shell]","CreateViewWindow method [Windows Shell]","IBrowserService2 interface","IBrowserService2 interface [Windows Shell]","CreateViewWindow method","IBrowserService2.CreateViewWindow","IBrowserService2::CreateViewWindow","shdeprecated/IBrowserService2::CreateViewWindow","shell.IBrowserService2_CreateViewWindow","zone_IBrowserService2_CreateViewWindow"]
old-location: shell\IBrowserService2_CreateViewWindow.htm
tech.root: shell
ms.assetid: f5e7f18b-86b3-4a30-bbb0-8c7f615c7186
ms.date: 12/05/2018
ms.keywords: CreateViewWindow, CreateViewWindow method [Windows Shell], CreateViewWindow method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],CreateViewWindow method, IBrowserService2.CreateViewWindow, IBrowserService2::CreateViewWindow, shdeprecated/IBrowserService2::CreateViewWindow, shell.IBrowserService2_CreateViewWindow, zone_IBrowserService2_CreateViewWindow
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
 - IBrowserService2::CreateViewWindow
 - shdeprecated/IBrowserService2::CreateViewWindow
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
 - IBrowserService2.CreateViewWindow
---

# IBrowserService2::CreateViewWindow


## -description

Deprecated. Coordinates the updating of state when creating a new browser view window.

## -parameters

### -param psvNew [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> of the new browser window.

### -param psvOld [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> of the old browser window.

### -param prcView [out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the current dimensions of the browser view.

### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the new browser window handle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.