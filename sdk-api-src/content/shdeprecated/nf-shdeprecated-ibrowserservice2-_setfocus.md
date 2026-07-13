---
UID: NF:shdeprecated.IBrowserService2._SetFocus
title: IBrowserService2::_SetFocus (shdeprecated.h)
description: Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through TranslateAcceleratorSB or when IBrowserService2::v_MayGetNextToolbarFocus fails.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_SetFocus method","IBrowserService2._SetFocus","IBrowserService2::_SetFocus","_SetFocus","_SetFocus method [Windows Shell]","_SetFocus method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_SetFocus","shell.IBrowserService2__SetFocus","zone_IBrowserService2__SetFocus"]
old-location: shell\IBrowserService2__SetFocus.htm
tech.root: shell
ms.assetid: 4a69c3f4-49e0-4a06-8cf2-dc8db640f58f
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SetFocus method, IBrowserService2._SetFocus, IBrowserService2::_SetFocus, _SetFocus, _SetFocus method [Windows Shell], _SetFocus method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SetFocus, shell.IBrowserService2__SetFocus, zone_IBrowserService2__SetFocus
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
 - IBrowserService2::_SetFocus
 - shdeprecated/IBrowserService2::_SetFocus
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
 - IBrowserService2._SetFocus
---

# IBrowserService2::_SetFocus


## -description

Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a> or when <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus">IBrowserService2::v_MayGetNextToolbarFocus</a> fails.

## -parameters

### -param ptbi [in]

Type: <b>LPTOOLBARITEM</b>

A pointer to a [TOOLBARITEM](./ns-shdeprecated-toolbaritem.md) structure that specifies a browser toolbar item.

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the browser window in which the focus shift is taking place.

### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> that contains a keystroke message that indicates an accelerator.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.