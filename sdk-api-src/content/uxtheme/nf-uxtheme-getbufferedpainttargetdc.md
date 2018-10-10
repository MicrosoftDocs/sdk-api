---
UID: NF:uxtheme.GetBufferedPaintTargetDC
title: GetBufferedPaintTargetDC function
author: windows-sdk-content
description: Retrieves the target device context (DC).
old-location: controls\GetBufferedPaintTargetDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getbufferedpainttargetdc.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetBufferedPaintTargetDC, GetBufferedPaintTargetDC function [Windows Controls], _shell_GetBufferedPaintTargetDC, _shell_GetBufferedPaintTargetDC_cpp, controls.GetBufferedPaintTargetDC, controls._shell_GetBufferedPaintTargetDC, uxtheme/GetBufferedPaintTargetDC
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
---

# GetBufferedPaintTargetDC function


## -description


Retrieves the target device context (DC). 


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

A handle to the buffered paint context obtained through <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A handle to the requested DC, or <b>NULL</b> otherwise.




## -remarks



If successful, this function returns the target DC that was passed by the application to <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>. 



