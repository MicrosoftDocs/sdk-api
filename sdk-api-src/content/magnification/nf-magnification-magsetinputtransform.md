---
UID: NF:magnification.MagSetInputTransform
title: MagSetInputTransform function
author: windows-driver-content
description: Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.
old-location: magapi\magapi_magsetinputtransform.htm
old-project: magapi
ms.assetid: B42B59DB-9E21-4769-B605-014173514AEB
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: MagSetInputTransform, MagSetInputTransform function [Magnification API], magapi.magapi_magsetinputtransform, magnification/MagSetInputTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Magnification.dll
api_name:
-	MagSetInputTransform
product: Windows
targetos: Windows
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
---

# MagSetInputTransform function


## -description


Sets the current active input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.


## -parameters




### -param fEnabled [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE to enable input transformation, or FALSE to disable it.  


### -param pRectSource

TBD


### -param pRectDest

TBD




#### - prcDest [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

 The new destination rectangle, in unmagnified screen coordinates, that defines the area of the screen where the magnified screen content is displayed. Pen and touch input in this rectangle is mapped to the source rectangle. This parameter is ignored if <i>bEnabled</i> is FALSE.


#### - prcSource [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

 The new source rectangle, in unmagnified screen coordinates, that defines the area of the screen to magnify. This parameter is ignored if <i>bEnabled</i> is FALSE.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The input transformation maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space. This enables the system to pass pen and touch input that is entered in magnified screen content, to the correct UI element on the screen. For example, without input transformation, input is passed to the element located at the unmagnified screen coordinates, not to the item that appears in the magnified screen content. 

This function requires the calling process to have UIAccess privileges.  If the caller does not have UIAccess privileges, the call to <b>MagSetInputTransform</b> fails, and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns ERROR_ACCESS_DENIED. For more information, see <a href="https://msdn.microsoft.com/0c3689e1-2124-4142-b0bd-233e95ee1285">UI Automation Security Considerations</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=207612">/MANIFESTUAC (Embeds UAC information in manifest)</a>.


#### Examples

The following example sets the input transformation for the full-screen magnifier.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Applies an input transformation to adjust pen and touch input to account 
//   for the current magnification factor.
//
BOOL SetInputTranform()
{
    // Get the current magnification settings.
    float magLevel;
    int xOffset, yOffset;

    BOOL fResult = MagGetFullscreenTransform(&amp;magLevel, &amp;xOffset, &amp;yOffset);
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

        fResult = MagSetInputTransform(TRUE, &amp;rcSource, &amp;rcDest);
    }

    return fResult;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3825B5DB-BD25-4073-8EB3-65A57709A804">MagGetInputTransform</a>
 

 

