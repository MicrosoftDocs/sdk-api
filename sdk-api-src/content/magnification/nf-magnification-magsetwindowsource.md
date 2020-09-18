---
UID: NF:magnification.MagSetWindowSource
title: MagSetWindowSource function (magnification.h)
description: Sets the source rectangle for the magnification window.
helpviewer_keywords: ["MagSetWindowSource","MagSetWindowSource function [Magnification API]","magapi.magapi_MagSetWindowSource","magapi_MagSetWindowSource","magnification/MagSetWindowSource"]
old-location: magapi\magapi_MagSetWindowSource.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetwindowsource.htm
ms.date: 12/05/2018
ms.keywords: MagSetWindowSource, MagSetWindowSource function [Magnification API], magapi.magapi_MagSetWindowSource, magapi_MagSetWindowSource, magnification/MagSetWindowSource
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
 - MagSetWindowSource
 - magnification/MagSetWindowSource
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
 - MagSetWindowSource
---

# MagSetWindowSource function


## -description

Sets the source rectangle for the magnification window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

### -param rect [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The rectangle to be magnified, in desktop coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetwindowsource">MagGetWindowSource</a>