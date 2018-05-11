---
UID: NF:uxtheme.EndPanningFeedback
title: EndPanningFeedback function
author: windows-driver-content
description: Terminates any existing animation that was in process or set up by BeginPanningFeedback and UpdatePanningFeedback.
old-location: controls\EndPanningFeedback.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\endpanningfeedback.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: EndPanningFeedback, EndPanningFeedback function [Windows Controls], _controls_EndPanningFeedback, _controls_EndPanningFeedback_cpp, controls.EndPanningFeedback, controls._controls_EndPanningFeedback, uxtheme/EndPanningFeedback
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
api_name:
-	EndPanningFeedback
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# EndPanningFeedback function


## -description


Terminates any existing animation that was in process or set up by <a href="https://msdn.microsoft.com/b1da3ed7-68bd-4bf7-a951-ee85368ea1d3">BeginPanningFeedback</a> and <a href="https://msdn.microsoft.com/227631b3-33e8-4ade-a7ff-51b70aed9ec6">UpdatePanningFeedback</a>. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle to the target window that will receive feedback.


### -param fAnimateBack [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Flag that indicates whether the displaced window should return to the original position using animation. If <b>FALSE</b>, the method restore the moved window using a direct jump.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if successful.




## -remarks



This function can only be called after a <a href="https://msdn.microsoft.com/b1da3ed7-68bd-4bf7-a951-ee85368ea1d3">BeginPanningFeedback</a> call.



