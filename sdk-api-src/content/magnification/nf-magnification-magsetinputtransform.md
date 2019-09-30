---
UID: NF:magnification.MagSetInputTransform
title: MagSetInputTransform function (magnification.h)
author: windows-sdk-content
description: Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.
old-location: magapi\magapi_magsetinputtransform.htm
tech.root: magapi
ms.assetid: B42B59DB-9E21-4769-B605-014173514AEB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MagSetInputTransform, MagSetInputTransform function [Magnification API], magapi.magapi_magsetinputtransform, magnification/MagSetInputTransform
ms.topic: function
f1_keywords: 
 - "magnification/MagSetInputTransform"
req.header: magnification.h
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
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagSetInputTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MagSetInputTransform function


## -description


Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.


## -parameters




### -param fEnabled [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

TRUE to enable input transformation, or FALSE to disable it.  


### -param pRectSource [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">LPRECT</a></b>

 The new source rectangle, in unmagnified screen coordinates, that defines the area of the screen to magnify. This parameter is ignored if <i>bEnabled</i> is FALSE.


### -param pRectDest [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">LPRECT</a></b>

 The new destination rectangle, in unmagnified screen coordinates, that defines the area of the screen where the magnified screen content is displayed. Pen and touch input in this rectangle is mapped to the source rectangle. This parameter is ignored if <i>bEnabled</i> is FALSE.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The input transformation maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space. This enables the system to pass pen and touch input that is entered in magnified screen content, to the correct UI element on the screen. For example, without input transformation, input is passed to the element located at the unmagnified screen coordinates, not to the item that appears in the magnified screen content. 

This function requires the calling process to have UIAccess privileges.  If the caller does not have UIAccess privileges, the call to <b>MagSetInputTransform</b> fails, and the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns ERROR_ACCESS_DENIED. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-securityoverview">UI Automation Security Considerations</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=207612">/MANIFESTUAC (Embeds UAC information in manifest)</a>.


#### Examples

The following example sets the input transformation for the full-screen magnifier.


```cpp
// Description:
//   Applies an input transformation to adjust pen and touch input to account 
//   for the current magnification factor.
//
BOOL SetInputTranform()
{
    // Get the current magnification settings.
    float magLevel;
    int xOffset, yOffset;

    BOOL fResult = MagGetFullscreenTransform(&magLevel, &xOffset, &yOffset);
    if (fResult)
    {
        // Assume that pen or touch input occurs only in the primary monitor.
        RECT rcDest;
        rcDest.left   = 0;
        rcDest.top    = 0;
        rcDest.right  = GetSystemMetrics(SM_CXSCREEN);
        rcDest.bottom = GetSystemMetrics(SM_CYSCREEN);

        // Calculate the portion of the screen that is visible in the magnified
        // view.
        RECT rcSource;
        rcSource.left   = xOffset;
        rcSource.top    = yOffset;
        rcSource.right  = rcSource.left + (int)(rcDest.right / magLevel);
        rcSource.bottom = rcSource.top  + (int)(rcDest.bottom / magLevel);

        fResult = MagSetInputTransform(TRUE, &rcSource, &rcDest);
    }

    return fResult;
}

```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetinputtransform">MagGetInputTransform</a>
 

 

