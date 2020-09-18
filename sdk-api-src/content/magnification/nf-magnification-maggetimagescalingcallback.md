---
UID: NF:magnification.MagGetImageScalingCallback
title: MagGetImageScalingCallback function (magnification.h)
description: Retrieves the registered callback function that implements a custom transform for image scaling.
helpviewer_keywords: ["MagGetImageScalingCallback","MagGetImageScalingCallback function [Magnification API]","magapi.magapi_MagGetImageScalingCallback","magapi_MagGetImageScalingCallback","magnification/MagGetImageScalingCallback"]
old-location: magapi\magapi_MagGetImageScalingCallback.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetimagescalingcallback.htm
ms.date: 12/05/2018
ms.keywords: MagGetImageScalingCallback, MagGetImageScalingCallback function [Magnification API], magapi.magapi_MagGetImageScalingCallback, magapi_MagGetImageScalingCallback, magnification/MagGetImageScalingCallback
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
 - MagGetImageScalingCallback
 - magnification/MagGetImageScalingCallback
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
 - MagGetImageScalingCallback
---

# MagGetImageScalingCallback function


## -description

<div class="alert"><b>Note</b>  The <b>MagGetImageScalingCallback</b> function is deprecated in Windows 7 and later, and should not be used in new applications.  There is no alternate functionality.</div>
<div> </div>


Retrieves the registered callback function that implements a custom transform for image scaling.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

## -returns

Type: <b><a href="/previous-versions/windows/desktop/api/magnification/nc-magnification-magimagescalingcallback">MagImageScalingCallback</a></b>

Returns the registered <a href="/previous-versions/windows/desktop/api/magnification/nc-magnification-magimagescalingcallback">MagImageScalingCallback</a> callback function, or <b>NULL</b> if no callback is registered.

## -remarks

This function returns <b>NULL</b> if Windows Display Driver Model (WDDM) is not supported.

This function works only when <a href="/windows/desktop/dwm/dwm-overview">Desktop Window Manager</a> (DWM) is off.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nc-magnification-magimagescalingcallback">MagImageScalingCallback</a>



<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetimagescalingcallback">MagSetImageScalingCallback</a>