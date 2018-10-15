---
UID: NF:uxtheme.BufferedPaintUnInit
title: BufferedPaintUnInit function
author: windows-sdk-content
description: Closes down buffered painting for the current thread. Called once for each call to BufferedPaintInit after calls to BeginBufferedPaint are no longer needed.
old-location: controls\BufferedPaintUnInit.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintuninit.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: BufferedPaintUnInit, BufferedPaintUnInit function [Windows Controls], _shell_BufferedPaintUnInit, _shell_BufferedPaintUnInit_cpp, controls.BufferedPaintUnInit, controls._shell_BufferedPaintUnInit, uxtheme/BufferedPaintUnInit
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
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - BufferedPaintUnInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BufferedPaintUnInit function


## -description


Closes down buffered painting for the current thread. Called once for each call to <a href="https://msdn.microsoft.com/e35fd59a-f493-4ac0-971a-d0746123e255">BufferedPaintInit</a> after calls to <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a> are no longer needed.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



