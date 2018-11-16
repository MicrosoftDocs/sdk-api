---
UID: NF:uxtheme.BufferedPaintStopAllAnimations
title: BufferedPaintStopAllAnimations function
author: windows-sdk-content
description: Stops all buffered animations for the given window.
old-location: controls\BufferedPaintStopAllAnimations.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintstopallanimations.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: BufferedPaintStopAllAnimations, BufferedPaintStopAllAnimations function [Windows Controls], _shell_BufferedPaintStopAllAnimations, _shell_BufferedPaintStopAllAnimations_cpp, controls.BufferedPaintStopAllAnimations, controls._shell_BufferedPaintStopAllAnimations, uxtheme/BufferedPaintStopAllAnimations
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
 - BufferedPaintStopAllAnimations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BufferedPaintStopAllAnimations
: 
---

# BufferedPaintStopAllAnimations function


## -description


Stops all buffered animations for the given window.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window in which to stop all animations.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



