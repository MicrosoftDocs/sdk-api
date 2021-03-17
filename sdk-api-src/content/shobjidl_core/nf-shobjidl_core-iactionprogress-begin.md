---
UID: NF:shobjidl_core.IActionProgress.Begin
title: IActionProgress::Begin (shobjidl_core.h)
description: Called when an action has begun that requires its progress be displayed to the user.
helpviewer_keywords: ["Begin","Begin method [Windows Shell]","Begin method [Windows Shell]","IActionProgress interface","IActionProgress interface [Windows Shell]","Begin method","IActionProgress.Begin","IActionProgress::Begin","shell.IActionProgress_Begin","shell_IActionProgress_Begin","shobjidl_core/IActionProgress::Begin"]
old-location: shell\IActionProgress_Begin.htm
tech.root: shell
ms.assetid: c26dd072-6d59-4c6c-a273-682ded994612
ms.date: 12/05/2018
ms.keywords: Begin, Begin method [Windows Shell], Begin method [Windows Shell],IActionProgress interface, IActionProgress interface [Windows Shell],Begin method, IActionProgress.Begin, IActionProgress::Begin, shell.IActionProgress_Begin, shell_IActionProgress_Begin, shobjidl_core/IActionProgress::Begin
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shobjidl.idl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActionProgress::Begin
 - shobjidl_core/IActionProgress::Begin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.idl
api_name:
 - IActionProgress.Begin
---

# IActionProgress::Begin


## -description

Called when an action has begun that requires its progress be displayed to the user.

## -parameters

### -param action [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction">SPACTION</a></b>

The action being performed. See <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction">SPACTION</a> for a list of acceptable values.

### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_spbeginf">SPBEGINF</a></b>

Optional flags that request certain UI operations be enabled or disabled. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_spbeginf">SPBEGINF</a> for a list of acceptable values.

## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.

## -remarks

This method should be called when an action is beginning. The values of <i>action</i> and <i>flags</i> may be used to determine how to draw the UI that will be displayed to the user, or how to interpret or filter certain user actions associated with the action. When the action has completed, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-end">IActionProgress::End</a> should be called.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-end">IActionProgress::End</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction">SPACTION</a>



<a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_spbeginf">SPBEGINF</a>