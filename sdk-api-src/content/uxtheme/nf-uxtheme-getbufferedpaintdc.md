---
UID: NF:uxtheme.GetBufferedPaintDC
title: GetBufferedPaintDC function (uxtheme.h)
description: Gets the paint device context (DC). This is the same value retrieved by BeginBufferedPaint.
helpviewer_keywords: ["GetBufferedPaintDC","GetBufferedPaintDC function [Windows Controls]","_shell_GetBufferedPaintDC","_shell_GetBufferedPaintDC_cpp","controls.GetBufferedPaintDC","controls._shell_GetBufferedPaintDC","uxtheme/GetBufferedPaintDC"]
old-location: controls\GetBufferedPaintDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpaintdc.htm
ms.date: 12/05/2018
ms.keywords: GetBufferedPaintDC, GetBufferedPaintDC function [Windows Controls], _shell_GetBufferedPaintDC, _shell_GetBufferedPaintDC_cpp, controls.GetBufferedPaintDC, controls._shell_GetBufferedPaintDC, uxtheme/GetBufferedPaintDC
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
req.lib: Uxtheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetBufferedPaintDC
 - uxtheme/GetBufferedPaintDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetBufferedPaintDC
---

# GetBufferedPaintDC function


## -description

Gets the paint device context (DC). This is the same value retrieved by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -parameters

### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

Handle of the buffered paint context, obtained through <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Handle of the requested DC. This is the same DC that is returned by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>. Returns <b>NULL</b> upon failure.