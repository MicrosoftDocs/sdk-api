---
UID: NF:uxtheme.GetBufferedPaintTargetRect
title: GetBufferedPaintTargetRect function (uxtheme.h)
description: Retrieves the target rectangle specified by BeginBufferedPaint.
helpviewer_keywords: ["GetBufferedPaintTargetRect","GetBufferedPaintTargetRect function [Windows Controls]","_shell_GetBufferedPaintTargetRect","_shell_GetBufferedPaintTargetRect_cpp","controls.GetBufferedPaintTargetRect","controls._shell_GetBufferedPaintTargetRect","uxtheme/GetBufferedPaintTargetRect"]
old-location: controls\GetBufferedPaintTargetRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpainttargetrect.htm
ms.date: 12/05/2018
ms.keywords: GetBufferedPaintTargetRect, GetBufferedPaintTargetRect function [Windows Controls], _shell_GetBufferedPaintTargetRect, _shell_GetBufferedPaintTargetRect_cpp, controls.GetBufferedPaintTargetRect, controls._shell_GetBufferedPaintTargetRect, uxtheme/GetBufferedPaintTargetRect
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
 - GetBufferedPaintTargetRect
 - uxtheme/GetBufferedPaintTargetRect
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
 - GetBufferedPaintTargetRect
---

# GetBufferedPaintTargetRect function


## -description

Retrieves the target rectangle specified by BeginBufferedPaint.

## -parameters

### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

Handle to the buffered paint context obtained through <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

### -param prc [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

When this function returns, contains the requested rectangle.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this function fails, the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure at <i>prc</i> is set to empty.