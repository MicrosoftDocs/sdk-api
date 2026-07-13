---
UID: NF:uxtheme.GetThemeTimingFunction
title: GetThemeTimingFunction function (uxtheme.h)
description: Gets a predefined timing function based on a timing function identifier.
helpviewer_keywords: ["GetThemeTimingFunction","GetThemeTimingFunction function [Windows Controls]","controls.getthemetimingfunction","uxtheme/GetThemeTimingFunction"]
old-location: controls\getthemetimingfunction.htm
tech.root: Controls
ms.assetid: 640E1933-E23D-4852-95A2-4FD630162D2C
ms.date: 12/05/2018
ms.keywords: GetThemeTimingFunction, GetThemeTimingFunction function [Windows Controls], controls.getthemetimingfunction, uxtheme/GetThemeTimingFunction
req.header: uxtheme.h
req.include-header: 
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeTimingFunction
 - uxtheme/GetThemeTimingFunction
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeTimingFunction
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

