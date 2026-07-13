---
UID: NF:winuser.DefRawInputProc
title: DefRawInputProc function (winuser.h)
description: Verifies that the size of the RAWINPUTHEADER structure is correct.
helpviewer_keywords: ["DefRawInputProc","DefRawInputProc function [Keyboard and Mouse Input]","_win32_DefRawInputProc","_win32_defrawinputproc_cpp","inputdev.defrawinputproc","winui._win32_defrawinputproc","winuser/DefRawInputProc"]
old-location: inputdev\defrawinputproc.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\defrawinputproc.htm
ms.date: 12/05/2018
ms.keywords: DefRawInputProc, DefRawInputProc function [Keyboard and Mouse Input], _win32_DefRawInputProc, _win32_defrawinputproc_cpp, inputdev.defrawinputproc, winui._win32_defrawinputproc, winuser/DefRawInputProc
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DefRawInputProc
 - winuser/DefRawInputProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-rawinput-l1-2-0.dll
 - ext-ms-win-rtcore-ntuser-rawinput-l1-1-1.dll
 - ext-ms-win-ntuser-rawinput-l1-2-0.dll
 - User32.dll
api_name:
 - DefRawInputProc
req.apiset: ext-ms-win-ntuser-rawinput-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DefRawInputProc function


## -description

Unlike <a href="/windows/win32/api/winuser/nf-winuser-defwindowproca">DefWindowProcA</a> and <a href="/windows/win32/api/winuser/nf-winuser-defwindowprocw">DefWindowProcW</a>, this function doesn't do any processing.

<b>DefRawInputProc</b> only checks whether <b>cbSizeHeader</b>'s value corresponds to the expected size of <a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>.

## -parameters

### -param paRawInput [in]

Type: <b>PRAWINPUT*</b>

Ignored.

### -param nInput [in]

Type: <b>INT</b>

Ignored.

### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a> structure.

## -returns

Type: <b>LRESULT</b>

If successful, the function returns <b>0</b>. Otherwise it returns <b>-1</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-rawinputheader">RAWINPUTHEADER</a>



<a href="/windows/desktop/inputdev/raw-input">Raw Input</a>
