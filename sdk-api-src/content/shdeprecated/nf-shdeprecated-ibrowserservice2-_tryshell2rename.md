---
UID: NF:shdeprecated.IBrowserService2._TryShell2Rename
title: IBrowserService2::_TryShell2Rename (shdeprecated.h)
description: Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_TryShell2Rename method","IBrowserService2._TryShell2Rename","IBrowserService2::_TryShell2Rename","_TryShell2Rename","_TryShell2Rename method [Windows Shell]","_TryShell2Rename method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_TryShell2Rename","shell.IBrowserService2__TryShell2Rename","zone_IBrowserService2__TryShell2Rename"]
old-location: shell\IBrowserService2__TryShell2Rename.htm
tech.root: shell
ms.assetid: 30801c5d-151b-4556-a1e5-1cbc81a5c33a
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_TryShell2Rename method, IBrowserService2._TryShell2Rename, IBrowserService2::_TryShell2Rename, _TryShell2Rename, _TryShell2Rename method [Windows Shell], _TryShell2Rename method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_TryShell2Rename, shell.IBrowserService2__TryShell2Rename, zone_IBrowserService2__TryShell2Rename
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
 - IBrowserService2::_TryShell2Rename
 - shdeprecated/IBrowserService2::_TryShell2Rename
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
 - IBrowserService2._TryShell2Rename
---

# IBrowserService2::_TryShell2Rename


## -description

Deprecated. Coordinates the renaming of the current browser view when the browser is redirected.

## -parameters

### -param psv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> representing the current browser view.

### -param pidlNew [in]

Type: <b>LPCITEMIDLIST</b>

A PIDL that indicates the new name of the browser view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called in response to <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-notifyredirect">NotifyRedirect</a>.