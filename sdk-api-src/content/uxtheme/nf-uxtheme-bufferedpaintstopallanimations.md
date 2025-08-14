---
UID: NF:uxtheme.BufferedPaintStopAllAnimations
title: BufferedPaintStopAllAnimations function (uxtheme.h)
description: Stops all buffered animations for the given window.
helpviewer_keywords: ["BufferedPaintStopAllAnimations","BufferedPaintStopAllAnimations function [Windows Controls]","_shell_BufferedPaintStopAllAnimations","_shell_BufferedPaintStopAllAnimations_cpp","controls.BufferedPaintStopAllAnimations","controls._shell_BufferedPaintStopAllAnimations","uxtheme/BufferedPaintStopAllAnimations"]
old-location: controls\BufferedPaintStopAllAnimations.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintstopallanimations.htm
ms.date: 12/05/2018
ms.keywords: BufferedPaintStopAllAnimations, BufferedPaintStopAllAnimations function [Windows Controls], _shell_BufferedPaintStopAllAnimations, _shell_BufferedPaintStopAllAnimations_cpp, controls.BufferedPaintStopAllAnimations, controls._shell_BufferedPaintStopAllAnimations, uxtheme/BufferedPaintStopAllAnimations
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
 - BufferedPaintStopAllAnimations
 - uxtheme/BufferedPaintStopAllAnimations
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
 - BufferedPaintStopAllAnimations
---

# BufferedPaintStopAllAnimations function


## -description

Stops all buffered animations for the given window.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window in which to stop all animations.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.