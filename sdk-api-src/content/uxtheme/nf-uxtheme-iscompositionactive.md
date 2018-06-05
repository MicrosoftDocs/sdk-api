---
UID: NF:uxtheme.IsCompositionActive
title: IsCompositionActive function
author: windows-sdk-content
description: Determines whether Desktop Window Manager (DWM) composition effects are available to the theme.
old-location: controls\IsCompositionActive.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\iscompositionactive.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IsCompositionActive, IsCompositionActive function [Windows Controls], _shell_IsCompositionActive, _shell_IsCompositionActive_cpp, controls.IsCompositionActive, controls._shell_IsCompositionActive, uxtheme/IsCompositionActive
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
-	xamlpalwp.dll
api_name:
-	IsCompositionActive
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# IsCompositionActive function


## -description


Determines whether Desktop Window Manager (DWM) composition effects are available to the theme.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if composition effects are available; otherwise, <b>FALSE</b>.




## -remarks



Composition effects are provided through the DWM. This function first determines whether DWM is active, then checks whether it has composition effects enabled.



