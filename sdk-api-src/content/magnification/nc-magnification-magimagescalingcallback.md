---
UID: NC:magnification.MagImageScalingCallback
title: MagImageScalingCallback (magnification.h)
description: Prototype for a callback function that implements a custom transform for image scaling.
helpviewer_keywords: ["MagImageScalingCallback","MagImageScalingCallback callback","MagImageScalingCallback callback function [Magnification API]","magapi.magapi_MagImageScalingCallback","magapi_MagImageScalingCallback","magnification/MagImageScalingCallback"]
old-location: magapi\magapi_MagImageScalingCallback.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magimagescalingcallback.htm
ms.date: 12/05/2018
ms.keywords: MagImageScalingCallback, MagImageScalingCallback callback, MagImageScalingCallback callback function [Magnification API], magapi.magapi_MagImageScalingCallback, magapi_MagImageScalingCallback, magnification/MagImageScalingCallback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MagImageScalingCallback
 - magnification/MagImageScalingCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Magnification.h
api_name:
 - MagImageScalingCallback
---

# MagImageScalingCallback callback function


## -description

<div class="alert"><b>Note</b>  The <i>MagImageScalingCallback</i> function is deprecated in Windows 7 and later, and should not be used in new applications.  There is no alternate functionality.</div><div> </div>Prototype for a callback function that implements a custom transform for image scaling.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

### -param srcdata [in]

Type: <b>void*</b>

The input data.

### -param srcheader [in]

Type: <b><a href="/windows/desktop/api/magnification/ns-magnification-magimageheader">MAGIMAGEHEADER</a></b>

The description of the input format.

### -param destdata [out]

Type: <b>void*</b>

The output data.

### -param destheader [in]

Type: <b><a href="/windows/desktop/api/magnification/ns-magnification-magimageheader">MAGIMAGEHEADER</a></b>

The description of the output format.

### -param unclipped [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates of the scaled version of the source bitmap.

### -param clipped [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates of the window to which the scaled bitmap is clipped.

### -param dirty [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRGN</a></b>

The region that needs to be refreshed.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/magnification/ns-magnification-magimageheader">MAGIMAGEHEADER</a>



<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetimagescalingcallback">MagGetImageScalingCallback</a>
