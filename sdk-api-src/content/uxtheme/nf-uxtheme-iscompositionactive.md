---
UID: NF:uxtheme.IsCompositionActive
title: IsCompositionActive function (uxtheme.h)
description: Determines whether Desktop Window Manager (DWM) composition effects are available to the theme.
helpviewer_keywords: ["IsCompositionActive","IsCompositionActive function [Windows Controls]","_shell_IsCompositionActive","_shell_IsCompositionActive_cpp","controls.IsCompositionActive","controls._shell_IsCompositionActive","uxtheme/IsCompositionActive"]
old-location: controls\IsCompositionActive.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\iscompositionactive.htm
ms.date: 12/05/2018
ms.keywords: IsCompositionActive, IsCompositionActive function [Windows Controls], _shell_IsCompositionActive, _shell_IsCompositionActive_cpp, controls.IsCompositionActive, controls._shell_IsCompositionActive, uxtheme/IsCompositionActive
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
 - IsCompositionActive
 - uxtheme/IsCompositionActive
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
 - IsCompositionActive
---

# IsCompositionActive function


## -description

Determines whether Desktop Window Manager (DWM) composition effects are available to the theme.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if composition effects are available; otherwise, <b>FALSE</b>.

## -remarks

Composition effects are provided through the DWM. This function first determines whether DWM is active, then checks whether it has composition effects enabled.
