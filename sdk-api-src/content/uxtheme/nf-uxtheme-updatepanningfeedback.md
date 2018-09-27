---
UID: NF:uxtheme.UpdatePanningFeedback
title: UpdatePanningFeedback function
author: windows-sdk-content
description: Updates clients about state of a window resulting from a panning gesture. This function can only be called after a BeginPanningFeedback call.
old-location: controls\UpdatePanningFeedback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\updatepanningfeedback.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: UpdatePanningFeedback, UpdatePanningFeedback function [Windows Controls], _controls_UpdatePanningFeedback, _controls_UpdatePanningFeedback_cpp, controls.UpdatePanningFeedback, controls._controls_UpdatePanningFeedback, uxtheme/UpdatePanningFeedback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - UpdatePanningFeedback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UpdatePanningFeedback function


## -description


Updates clients about state of a window resulting from a panning gesture. This function can only be called after a <a href="https://msdn.microsoft.com/en-us/library/Dd373383(v=VS.85).aspx">BeginPanningFeedback</a> call.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle to the target window that will receive feedback. For the method to succeed, this must be the same HWND as provided in <a href="https://msdn.microsoft.com/en-us/library/Dd373383(v=VS.85).aspx">BeginPanningFeedback</a>. 


### -param lTotalOverpanOffsetX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The total displacement that the window has moved in the horizontal direction since the end of scrollable region was reached. A maximum displacement of 30 pixels is allowed.


### -param lTotalOverpanOffsetY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The total displacement that the window has moved in the vertical direction since the end of scrollable region was reached. A maximum displacement of 30 pixels is allowed.


### -param fInInertia [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Flag indicating whether the application is handling a WM_GESTURE message with the GF_INERTIA FLAG set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if successful.




## -remarks



Incremental calls to this function should always pass the sum of the increments and not just the latest increment itself.



