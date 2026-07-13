---
UID: NF:immdev.ImmAssociateContext
title: ImmAssociateContext function (immdev.h)
description: The ImmAssociateContext function (immdev.h) associates the specified input context with the specified window.
helpviewer_keywords: ["ImmAssociateContext","ImmAssociateContext function [Internationalization for Windows Applications]","_win32_ImmAssociateContext","imm/ImmAssociateContext","intl.immassociatecontext"]
old-location: intl\immassociatecontext.htm
tech.root: Intl
ms.assetid: 978ea304-c44d-4f00-b86f-932bbd5f603c
ms.date: 08/04/2022
ms.keywords: ImmAssociateContext, ImmAssociateContext function [Internationalization for Windows Applications], _win32_ImmAssociateContext, imm/ImmAssociateContext, intl.immassociatecontext
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmAssociateContext
 - immdev/ImmAssociateContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmAssociateContext
---

# ImmAssociateContext function


## -description

Associates the specified input context with the specified window. By default, the operating system associates the default input context with each window as it is created.
<div class="alert"><b>Note</b>  To specify a type of association, the application should use the <a href="/windows/desktop/api/imm/nf-imm-immassociatecontextex">ImmAssociateContextEx</a> function.</div><div> </div>

## -parameters

### -param HWND [in]

Handle to the window to associate with the input context.

### -param HIMC [in]

Handle to the input context. If <i>hIMC</i> is <b>NULL</b>, the function removes any association the window has with an input context. Thus IME cannot be used in the window.

## -returns

Returns the handle to the input context previously associated with the window.

## -remarks

When associating an input context with a window, an application must remove the association before destroying the input context. One way to do this is to save the handle and reassociate it to the default input context with the window.

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immassociatecontextex">ImmAssociateContextEx</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
