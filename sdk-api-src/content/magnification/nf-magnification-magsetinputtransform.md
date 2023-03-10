---
UID: NF:magnification.MagSetInputTransform
title: MagSetInputTransform function (magnification.h)
description: Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.
old-location: magapi\magapi_magsetinputtransform.htm
tech.root: magapi
ms.assetid: B42B59DB-9E21-4769-B605-014173514AEB
ms.date: 12/05/2018
ms.keywords: MagSetInputTransform, MagSetInputTransform function [Magnification API], magapi.magapi_magsetinputtransform, magnification/MagSetInputTransform
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MagSetInputTransform
 - magnification/MagSetInputTransform
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
 - MagSetInputTransform
---

# MagSetInputTransform function


## -description

Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.

## -parameters

### -param fEnabled [in]

Type: **[BOOL](/windows/win32/WinProg/windows-data-types)**

TRUE to enable input transformation, or FALSE to disable it.

### -param pRectSource [in]

Type: **const [LPRECT](../windef/ns-windef-rect.md)**

 The new source rectangle, in unmagnified screen coordinates, that defines the area of the screen to magnify. This parameter is ignored if *bEnabled* is FALSE.

### -param pRectDest [in]

Type: **const [LPRECT](../windef/ns-windef-rect.md)**

 The new destination rectangle, in unmagnified screen coordinates, that defines the area of the screen where the magnified screen content is displayed. Pen and touch input in this rectangle is mapped to the source rectangle. This parameter is ignored if *bEnabled* is FALSE.

## -returns

Type: **[BOOL](/windows/win32/WinProg/windows-data-types)**

Returns TRUE if successful, or FALSE otherwise.

## -remarks

The input transformation maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space. This enables the system to pass pen and touch input that is entered in magnified screen content, to the correct UI element on the screen. For example, without input transformation, input is passed to the element located at the unmagnified screen coordinates, not to the item that appears in the magnified screen content.

This function requires the calling process to have UIAccess privileges.  If the caller does not have UIAccess privileges, the call to **MagSetInputTransform** fails, and the [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) function returns ERROR_ACCESS_DENIED. For more information, see [UI Automation Security Considerations](/windows/win32/WinAuto/uiauto-securityoverview) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

Beginning with Windows 10 Creators Update (version 1703), you must use the [MagSetInputTransform function](nf-magnification-magsetinputtransform.md) for mouse input to route to the magnified element (in addition to pen and touch input).

## Examples

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

[MagGetFullscreenTransform](./nf-magnification-maggetfullscreentransform.md)