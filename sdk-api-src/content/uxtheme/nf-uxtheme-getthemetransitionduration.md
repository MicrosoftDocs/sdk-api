---
UID: NF:uxtheme.GetThemeTransitionDuration
title: GetThemeTransitionDuration function
author: windows-sdk-content
description: Gets the duration for the specified transition.
old-location: controls\GetThemeTransitionDuration.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetransitionduration.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetThemeTransitionDuration, GetThemeTransitionDuration function [Windows Controls], _shell_GetThemeTransitionDuration, _shell_GetThemeTransitionDuration_cpp, controls.GetThemeTransitionDuration, controls._shell_GetThemeTransitionDuration, uxtheme/GetThemeTransitionDuration
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
 - GetThemeTransitionDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Address of a variable that receives the transition duration, in milliseconds.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



