---
UID: NF:uxtheme.GetBufferedPaintDC
title: GetBufferedPaintDC function (uxtheme.h)
author: windows-sdk-content
description: Gets the paint device context (DC). This is the same value retrieved by BeginBufferedPaint.
old-location: controls\GetBufferedPaintDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpaintdc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBufferedPaintDC, GetBufferedPaintDC function [Windows Controls], _shell_GetBufferedPaintDC, _shell_GetBufferedPaintDC_cpp, controls.GetBufferedPaintDC, controls._shell_GetBufferedPaintDC, uxtheme/GetBufferedPaintDC
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetBufferedPaintDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetBufferedPaintDC function


## -description


Gets the paint device context (DC). This is the same value retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

Handle of the buffered paint context, obtained through <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Handle of the requested DC. This is the same DC that is returned by <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>. Returns <b>NULL</b> upon failure.



