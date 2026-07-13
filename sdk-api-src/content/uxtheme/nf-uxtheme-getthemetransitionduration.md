---
UID: NF:uxtheme.GetThemeTransitionDuration
title: GetThemeTransitionDuration function (uxtheme.h)
description: Gets the duration for the specified transition.
helpviewer_keywords: ["GetThemeTransitionDuration","GetThemeTransitionDuration function [Windows Controls]","_shell_GetThemeTransitionDuration","_shell_GetThemeTransitionDuration_cpp","controls.GetThemeTransitionDuration","controls._shell_GetThemeTransitionDuration","uxtheme/GetThemeTransitionDuration"]
old-location: controls\GetThemeTransitionDuration.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetransitionduration.htm
ms.date: 12/05/2018
ms.keywords: GetThemeTransitionDuration, GetThemeTransitionDuration function [Windows Controls], _shell_GetThemeTransitionDuration, _shell_GetThemeTransitionDuration_cpp, controls.GetThemeTransitionDuration, controls._shell_GetThemeTransitionDuration, uxtheme/GetThemeTransitionDuration
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
req.lib: Uxtheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeTransitionDuration
 - uxtheme/GetThemeTransitionDuration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeTransitionDuration
---

# GetThemeTransitionDuration function


## -description

Gets the duration for the specified transition.

## -parameters

### -param hTheme

Type: <b>HTHEME</b>

Handle of the theme data.

### -param iPartId

Type: <b>int</b>

ID of the part.

### -param iStateIdFrom

Type: <b>int</b>

State ID of the part before the transition.

### -param iStateIdTo

Type: <b>int</b>

State ID of the part after the transition.

### -param iPropId

Type: <b>int</b>

Property ID.

### -param pdwDuration [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Address of a variable that receives the transition duration, in milliseconds.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.