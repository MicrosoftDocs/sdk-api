---
UID: NF:uxtheme.BeginPanningFeedback
title: BeginPanningFeedback function
author: windows-sdk-content
description: Notifies the system to send feedback about a target window affected by panning gestures.
old-location: controls\BeginPanningFeedback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\beginpanningfeedback.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: BeginPanningFeedback, BeginPanningFeedback function [Windows Controls], _controls_BeginPanningFeedback, _controls_BeginPanningFeedback_cpp, controls.BeginPanningFeedback, controls._controls_BeginPanningFeedback, uxtheme/BeginPanningFeedback
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
 - BeginPanningFeedback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BeginPanningFeedback function


## -description


Notifies the system to send feedback about a target window affected by panning gestures. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle to the target window that will receive feedback.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE, if successful.




## -remarks



This function must be called before either the <a href="https://msdn.microsoft.com/227631b3-33e8-4ade-a7ff-51b70aed9ec6">UpdatePanningFeedback</a> or <a href="https://msdn.microsoft.com/38e72b4e-5614-44f5-bc68-b25c96396494">EndPanningFeedback</a> functions can be called.



