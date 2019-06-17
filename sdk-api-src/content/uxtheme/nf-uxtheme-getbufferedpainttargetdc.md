---
UID: NF:uxtheme.GetBufferedPaintTargetDC
title: GetBufferedPaintTargetDC function (uxtheme.h)
author: windows-sdk-content
description: Retrieves the target device context (DC).
old-location: controls\GetBufferedPaintTargetDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpainttargetdc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBufferedPaintTargetDC, GetBufferedPaintTargetDC function [Windows Controls], _shell_GetBufferedPaintTargetDC, _shell_GetBufferedPaintTargetDC_cpp, controls.GetBufferedPaintTargetDC, controls._shell_GetBufferedPaintTargetDC, uxtheme/GetBufferedPaintTargetDC
ms.topic: function
f1_keywords: ["uxtheme/GetBufferedPaintTargetDC"]
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
 - GetBufferedPaintTargetDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetBufferedPaintTargetDC function


## -description


Retrieves the target device context (DC). 


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

A handle to the buffered paint context obtained through <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HDC</a></b>

A handle to the requested DC, or <b>NULL</b> otherwise.




## -remarks



If successful, this function returns the target DC that was passed by the application to <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>. 



