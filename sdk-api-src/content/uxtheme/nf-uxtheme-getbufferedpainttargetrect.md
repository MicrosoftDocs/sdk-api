---
UID: NF:uxtheme.GetBufferedPaintTargetRect
title: GetBufferedPaintTargetRect function
author: windows-driver-content
description: Retrieves the target rectangle specified by BeginBufferedPaint.
old-location: controls\GetBufferedPaintTargetRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpainttargetrect.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetBufferedPaintTargetRect, GetBufferedPaintTargetRect function [Windows Controls], _shell_GetBufferedPaintTargetRect, _shell_GetBufferedPaintTargetRect_cpp, controls.GetBufferedPaintTargetRect, controls._shell_GetBufferedPaintTargetRect, uxtheme/GetBufferedPaintTargetRect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
api_name:
-	GetBufferedPaintTargetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetBufferedPaintTargetRect function


## -description


Retrieves the target rectangle specified by BeginBufferedPaint.


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

Handle to the buffered paint context obtained through <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


### -param prc [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

When this function returns, contains the requested rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this function fails, the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure at <i>prc</i> is set to empty.



