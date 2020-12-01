---
UID: NF:magnification.MagSetFullscreenTransform
title: MagSetFullscreenTransform function (magnification.h)
description: Changes the magnification settings for the full-screen magnifier.
old-location: magapi\magapi_magsetfullscreentransform.htm
tech.root: magapi
ms.assetid: B02C2A37-6BA6-4DF8-92C1-748BF7B25B96
ms.date: 12/05/2018
ms.keywords: MagSetFullscreenTransform, MagSetFullscreenTransform function [Magnification API], magapi.magapi_magsetfullscreentransform, magnification/MagSetFullscreenTransform
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
 - MagSetFullscreenTransform
 - magnification/MagSetFullscreenTransform
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
 - MagSetFullscreenTransform
---

# MagSetFullscreenTransform function


## -description

Changes the magnification settings for the full-screen magnifier.

## -parameters

### -param magLevel [in]

Type: **float**

The new magnification factor for the full-screen magnifier.  The minimum value of this parameter is 1.0, and the maximum value is 4096.0. If this value is 1.0, the screen content is not magnified and no offsets are applied.

### -param xOffset [in]

Type: **int**

The new x-coordinate offset, in pixels, for the upper-left corner of the magnified view. The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates. The minimum value of the parameter is -262144, and the maximum value is 262144.

### -param yOffset [in]

Type: **int**

The new y-coordinate offset, in pixels, for the upper-left corner of the magnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates. The minimum value of the parameter is -262144, and the maximum value is 262144.

## -returns

Type: **BOOL**

Returns TRUE if successful. Otherwise, FALSE.

## -remarks

The offsets are not affected by the current dots per inch (dpi) settings.

The magnification factor is applied to the current mouse cursor visuals, including cursor visuals affected by the mouse-related settings in the Ease of Access control panel.

In a multiple monitor environment, to position the upper-left corner of the magnified view to the left of the primary monitor, the offsets must be adjusted by the upper-left corner of the virtual screen and the magnification factor being applied. (The virtual screen is the bounding rectangle of all display monitors.) For an example that shows how to position the upper-left corner of the magnified view to the left of the primary monitor, see [Examples](#examples).

Beginning with Windows 10 Creators Update (version 1703), you must use the [MagSetInputTransform function](nf-magnification-magsetinputtransform.md) for input to route to the magnified element.

## Examples

The following example sets the magnification factor for the full-screen magnifier and places the center of  the magnified screen content at the center of the screen.

```cpp
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}

```

The following example magnifies the screen so that the upper-left corner of a particular window 
appears at the upper-left corner of the magnified view. If the <code>fPositionRelativeToVirtualScreen</code> parameter is FALSE, the window is positioned in the upper-left corner of the primary monitor. If <code>fPositionRelativeToVirtualScreen</code> is TRUE and the system has multiple monitors,  the example adjusts the offsets to position the window relative to the virtual screen; that is, the window is placed in the upper-left corner of the left-most monitor. 

```cpp
// Note: This example does not check whether the offset is large enough to 
// ensure that the magnified content fills the entire screen. Depending on the 
// location of the target window, some unmagnified content might be visible to 
// the right of the magnified content.

// Description:
//   Magnifies the screen such that the upper-left corner of a particular window 
//   appears at the upper-left corner of the magnified view.
//
// Parameters:
//   fPositionRelativeToVirtualDesktop - TRUE to set the magnified view relative
//   to the upper-left corner of the virtual screen, or FALSE to set the 
//   magnified view relative to the upper-left corner of the primary monitor.
//
BOOL SetFullscreenMagnification(BOOL fPositionRelativeToVirtualScreen)
{
    BOOL fResult = FALSE;

    // Get the window whose upper-left corner is to appear at the upper-left 
    // corner of the magnified view.
    HWND hWndTarget = FindWindow(L"TargetAppClass", NULL);
    if (hWndTarget != NULL)
    {
        RECT rcTarget;
        GetWindowRect(hWndTarget, &rcTarget);

        // Set the magnification to be 200%.
        float magVal = 2.0;

        // Position the point of interest to appear at the upper-left corner 
        // of the primary monitor.
        int xOffset = rcTarget.left;
        int yOffset = rcTarget.top;

        if (fPositionRelativeToVirtualScreen)
        {
            // Adjust the point of interest to appear at the upper-left corner of 
            // the virtual screen; that is, the left-most monitor.

            RECT rcVirtualScreen;
    
            rcVirtualScreen.left = GetSystemMetrics(SM_XVIRTUALSCREEN);
            rcVirtualScreen.top  = GetSystemMetrics(SM_YVIRTUALSCREEN);

            xOffset -= (int)(rcVirtualScreen.left / magVal);
            yOffset -= (int)(rcVirtualScreen.top  / magVal);
        }

        fResult = MagSetFullscreenTransform(magVal, xOffset, yOffset);
    }

    return fResult;
}

```

## -see-also

[MagGetFullscreenTransform](./nf-magnification-maggetfullscreentransform.md)