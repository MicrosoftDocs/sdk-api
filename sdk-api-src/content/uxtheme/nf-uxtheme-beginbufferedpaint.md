---
UID: NF:uxtheme.BeginBufferedPaint
title: BeginBufferedPaint function (uxtheme.h)
description: Begins a buffered paint operation.
helpviewer_keywords: ["BeginBufferedPaint","BeginBufferedPaint function [Windows Controls]","_shell_BeginBufferedPaint","_shell_BeginBufferedPaint_cpp","controls.BeginBufferedPaint","controls._shell_BeginBufferedPaint","uxtheme/BeginBufferedPaint"]
old-location: controls\BeginBufferedPaint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\beginbufferedpaint.htm
ms.date: 12/05/2018
ms.keywords: BeginBufferedPaint, BeginBufferedPaint function [Windows Controls], _shell_BeginBufferedPaint, _shell_BeginBufferedPaint_cpp, controls.BeginBufferedPaint, controls._shell_BeginBufferedPaint, uxtheme/BeginBufferedPaint
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BeginBufferedPaint
 - uxtheme/BeginBufferedPaint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - BeginBufferedPaint
---

# BeginBufferedPaint function


## -description

Begins a buffered paint operation.

## -parameters

### -param hdcTarget

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

The handle of the target DC on which the buffer will be painted.

### -param prcTarget

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the area of the target DC in which to paint.

### -param dwFormat

Type: <b><a href="/windows/desktop/api/uxtheme/ne-uxtheme-bp_bufferformat">BP_BUFFERFORMAT</a></b>

A member of the <a href="/windows/desktop/api/uxtheme/ne-uxtheme-bp_bufferformat">BP_BUFFERFORMAT</a> enumeration that specifies the format of the buffer.

### -param pPaintParams [in]

Type: <b><a href="/windows/desktop/api/uxtheme/ns-uxtheme-bp_paintparams">BP_PAINTPARAMS</a>*</b>

A pointer to a <a href="/windows/desktop/api/uxtheme/ns-uxtheme-bp_paintparams">BP_PAINTPARAMS</a> structure that defines the paint operation parameters. This value can be <b>NULL</b>.

### -param phdc [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a>*</b>

When this function returns, points to the handle of the new device context.

## -returns

Type: <b>HPAINTBUFFER</b>

A handle to the buffered paint context. If this function fails, the return value is <b>NULL</b>, and <i>phdc</i> is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The returned handle is freed when <a href="/windows/desktop/api/uxtheme/nf-uxtheme-endbufferedpaint">EndBufferedPaint</a> is called.

An application should call <a href="/windows/desktop/api/uxtheme/nf-uxtheme-bufferedpaintinit">BufferedPaintInit</a> on the calling thread before calling <b>BeginBufferedPaint</b>, and <a href="/windows/desktop/api/uxtheme/nf-uxtheme-bufferedpaintuninit">BufferedPaintUnInit</a> before the thread is terminated.  Failure to call <b>BufferedPaintInit</b> may result in degraded performance due to internal data being initialized and destroyed for each buffered paint operation.