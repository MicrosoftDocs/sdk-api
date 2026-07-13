---
UID: NF:shlobj_core.DAD_AutoScroll
title: DAD_AutoScroll function (shlobj_core.h)
description: Scrolls the window while an image is being dragged.
helpviewer_keywords: ["DAD_AutoScroll","DAD_AutoScroll function [Windows Shell]","shell.DAD_AutoScroll","shell_DAD_AutoScroll","shlobj_core/DAD_AutoScroll"]
old-location: shell\DAD_AutoScroll.htm
tech.root: shell
ms.assetid: 3c5af682-8497-477e-8222-3eb37d1e295f
ms.date: 12/05/2018
ms.keywords: DAD_AutoScroll, DAD_AutoScroll function [Windows Shell], shell.DAD_AutoScroll, shell_DAD_AutoScroll, shlobj_core/DAD_AutoScroll
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_AutoScroll
 - shlobj_core/DAD_AutoScroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - DAD_AutoScroll
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# DAD_AutoScroll function


## -description

<p class="CCE_Message">[<b>DAD_AutoScroll</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions.]

Scrolls the window while an image is being dragged.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window being scrolled.

### -param pad [in]

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data">AUTO_SCROLL_DATA</a>*</b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data">AUTO_SCROLL_DATA</a> structure.

### -param pptNow [in]

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to the current scroll coordinates.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

## -remarks

The function is successful and the window scrolls only when the <b>bFull</b> parameter of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data">AUTO_SCROLL_DATA</a> structure is <b>TRUE</b>. Each time this function is called, as long as <b>bFull</b> is <b>FALSE</b>, the <b>iNextSample</b> parameter is incremented by 1 and the current scroll coordinates and time are returned in the <b>AUTO_SCROLL_DATA</b> structure. When <b>iNextSample</b> is equal to NUM_POINTS, <b>bFull</b> is set to <b>TRUE</b>, the function succeeds, and the window scrolls.

## -see-also

<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data">AUTO_SCROLL_DATA</a>
