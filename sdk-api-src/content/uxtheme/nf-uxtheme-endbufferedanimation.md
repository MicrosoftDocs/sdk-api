---
UID: NF:uxtheme.EndBufferedAnimation
title: EndBufferedAnimation function
author: windows-sdk-content
description: Renders the first frame of a buffered animation operation and starts the animation timer.
old-location: controls\EndBufferedAnimation.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\endbufferedanimation.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EndBufferedAnimation, EndBufferedAnimation function [Windows Controls], _shell_EndBufferedAnimation, _shell_EndBufferedAnimation_cpp, controls.EndBufferedAnimation, controls._shell_EndBufferedAnimation, uxtheme/EndBufferedAnimation
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
 - EndBufferedAnimation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EndBufferedAnimation function


## -description


Renders the first frame of a buffered animation operation and starts the animation timer.


## -parameters




### -param hbpAnimation

Type: <b>HANIMATIONBUFFER</b>

The handle to the buffered animation context that was returned by <a href="https://msdn.microsoft.com/en-us/library/Bb773252(v=VS.85).aspx">BeginBufferedAnimation</a>.


### -param fUpdateTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, updates the target DC with the animation.  If <b>FALSE</b>, the animation is not started, the target DC is not updated, and the <i>hbpAnimation</i> parameter is freed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



