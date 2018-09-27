---
UID: NF:uxtheme.GetThemeTextMetrics
title: GetThemeTextMetrics function
author: windows-sdk-content
description: Retrieves information about the font specified by a visual style for a particular part.
old-location: controls\GetThemeTextMetrics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetextmetrics.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetThemeTextMetrics, GetThemeTextMetrics function [Windows Controls], controls.GetThemeTextMetrics, controls.inet_GetThemeTextMetrics, inet_GetThemeTextMetrics, inet_GetThemeTextMetrics_cpp, uxtheme/GetThemeTextMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
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
 - GetThemeTextMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThemeTextMetrics function


## -description


Retrieves information about the font specified by a visual style for a particular part.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use for screen context. This parameter may be set to <b>NULL</b>.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to retrieve font information about. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param ptm [out]

Type: <b><a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a>*</b>

Receives the font information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>
 

 

