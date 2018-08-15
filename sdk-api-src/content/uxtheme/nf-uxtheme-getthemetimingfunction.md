---
UID: NF:uxtheme.GetThemeTimingFunction
title: GetThemeTimingFunction function
author: windows-sdk-content
description: Gets a predefined timing function based on a timing function identifier.
old-location: controls\getthemetimingfunction.htm
old-project: controls
ms.assetid: 640E1933-E23D-4852-95A2-4FD630162D2C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetThemeTimingFunction, GetThemeTimingFunction function [Windows Controls], controls.getthemetimingfunction, uxtheme/GetThemeTimingFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeTimingFunction
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemeTimingFunction function


## -description


Gets a predefined timing function based on
a timing function identifier.


## -parameters




### -param hTheme [in]

An opened theme handle.


### -param iTimingFunctionId [in]

A timing function identifier.


### -param pTimingFunction [out]

A buffer to receive a predefined timing function pointer.


### -param cbSize [in]

The byte size of the buffer pointed by <i>pTimingFunction</i>.


### -param pcbSizeOut [out]

The byte size of
the timing function structure.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



