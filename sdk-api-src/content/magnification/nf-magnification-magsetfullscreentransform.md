---
UID: NF:magnification.MagSetFullscreenTransform
title: MagSetFullscreenTransform function
author: windows-sdk-content
description: Changes the magnification settings for the full-screen magnifier.
old-location: magapi\magapi_magsetfullscreentransform.htm
old-project: magapi
ms.assetid: B02C2A37-6BA6-4DF8-92C1-748BF7B25B96
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MagSetFullscreenTransform, MagSetFullscreenTransform function [Magnification API], magapi.magapi_magsetfullscreentransform, magnification/MagSetFullscreenTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: magnification.h
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
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagSetFullscreenTransform
product: Windows
targetos: Windows
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
---

# MagSetFullscreenTransform function


## -description


Changes the magnification settings for the full-screen magnifier.


## -parameters




### -param magLevel [in]

Type: <b>float</b>

The new magnification factor for the full-screen magnifier.  The minimum value of this parameter is 1.0, and the maximum value is 4096.0. If this value is 1.0, the screen content is not magnified and no offsets are applied.  


### -param xOffset [in]

Type: <b>int</b>

The new x-coordinate offset, in pixels, for the upper-left corner of the magnified view. The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates. The minimum value of the parameter is -262144, and the maximum value is 262144.


### -param yOffset [in]

Type: <b>int</b>

The new y-coordinate offset, in pixels, for the upper-left corner of the magnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates. The minimum value of the parameter is -262144, and the maximum value is 262144.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The offsets are not affected by the current dots per inch (dpi) settings.

The magnification factor is applied to the current mouse cursor visuals, including cursor visuals affected by the mouse-related settings in the Ease of Access control panel.

In a multiple monitor environment, to position the upper-left corner of the magnified view to the left of the primary monitor, the offsets must be adjusted by the upper-left corner of the virtual screen and the magnification factor being applied. (The virtual screen is the bounding rectangle of all display monitors.) For an example that shows how to position the upper-left corner of the magnified view to the left of the primary monitor, see Examples.




#### Examples

The following example sets the magnification factor for the full-screen magnifier and places the center of  the magnified screen content at the center of the screen.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor &lt; 1.0)
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
</pre>
</td>
</tr>
</table></span></div>
The following example magnifies the screen so that the upper-left corner of a particular window 
appears at the upper-left corner of the magnified view. If the <code>fPositionRelativeToVirtualScreen</code> parameter is FALSE, the window is positioned in the upper-left corner of the primary monitor. If <code>fPositionRelativeToVirtualScreen</code> is TRUE and the system has multiple monitors,  the example adjusts the offsets to position the window relative to the virtual screen; that is, the window is placed in the upper-left corner of the left-most monitor. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Note: This example does not check whether the offset is large enough to 
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
        GetWindowRect(hWndTarget, &amp;rcTarget);

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6270047A-8823-41D6-AD57-72A7E60F3696">MagGetFullscreenTransform</a>
 

 

