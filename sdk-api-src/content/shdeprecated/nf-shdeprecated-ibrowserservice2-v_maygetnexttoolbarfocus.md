---
UID: NF:shdeprecated.IBrowserService2.v_MayGetNextToolbarFocus
title: IBrowserService2::v_MayGetNextToolbarFocus (shdeprecated.h)
description: Deprecated. Used when translating accelerators through TranslateAcceleratorSB and in checking the cycle of focus between the view and the browser's toolbars.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","v_MayGetNextToolbarFocus method","IBrowserService2.v_MayGetNextToolbarFocus","IBrowserService2::v_MayGetNextToolbarFocus","shdeprecated/IBrowserService2::v_MayGetNextToolbarFocus","shell.IBrowserService2_v_MayGetNextToolbarFocus","v_MayGetNextToolbarFocus","v_MayGetNextToolbarFocus method [Windows Shell]","v_MayGetNextToolbarFocus method [Windows Shell]","IBrowserService2 interface","zone_IBrowserService2_v_MayGetNextToolbarFocus"]
old-location: shell\IBrowserService2_v_MayGetNextToolbarFocus.htm
tech.root: shell
ms.assetid: a1c271b2-d567-43b4-966e-0eea597f004b
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_MayGetNextToolbarFocus method, IBrowserService2.v_MayGetNextToolbarFocus, IBrowserService2::v_MayGetNextToolbarFocus, shdeprecated/IBrowserService2::v_MayGetNextToolbarFocus, shell.IBrowserService2_v_MayGetNextToolbarFocus, v_MayGetNextToolbarFocus, v_MayGetNextToolbarFocus method [Windows Shell], v_MayGetNextToolbarFocus method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_MayGetNextToolbarFocus
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
 - IBrowserService2::v_MayGetNextToolbarFocus
 - shdeprecated/IBrowserService2::v_MayGetNextToolbarFocus
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
 - IBrowserService2.v_MayGetNextToolbarFocus
---

# IBrowserService2::v_MayGetNextToolbarFocus


## -description

Deprecated. Used when translating accelerators through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a> and in checking the cycle of focus between the view and the browser's toolbars.

## -parameters

### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> that contains the keystroke message.

### -param itbNext [in]

Type: <b>UINT</b>

The index of the next toolbar, or ITB_VIEW if focus is shifting to the view.

### -param citb [in]

Type: <b>int</b>

The ID of the current toolbar with focus, or ITB_VIEW if the view has focus.

### -param pptbi [out]

Type: <b>LPTOOLBARITEM*</b>

A pointer to a [TOOLBARITEM](./ns-shdeprecated-toolbaritem.md) structure that represents the toolbar receiving the focus.

### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the handle of the window that contains the toolbar.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.