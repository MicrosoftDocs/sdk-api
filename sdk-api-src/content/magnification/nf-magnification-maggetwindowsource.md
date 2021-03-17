---
UID: NF:magnification.MagGetWindowSource
title: MagGetWindowSource function (magnification.h)
description: Gets the rectangle of the area that is being magnified.
helpviewer_keywords: ["MagGetWindowSource","MagGetWindowSource function [Magnification API]","magapi.magapi_MagGetWindowSource","magapi_MagGetWindowSource","magnification/MagGetWindowSource"]
old-location: magapi\magapi_MagGetWindowSource.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowsource.htm
ms.date: 12/05/2018
ms.keywords: MagGetWindowSource, MagGetWindowSource function [Magnification API], magapi.magapi_MagGetWindowSource, magapi_MagGetWindowSource, magnification/MagGetWindowSource
req.header: magnification.h
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
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MagGetWindowSource
 - magnification/MagGetWindowSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagGetWindowSource
---

# MagGetWindowSource function


## -description

Gets the rectangle of the area that is being magnified.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

### -param pRect [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The rectangle that is being magnified, in desktop coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetwindowsource">MagSetWindowSource</a>