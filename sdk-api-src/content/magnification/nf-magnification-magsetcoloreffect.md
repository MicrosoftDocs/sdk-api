---
UID: NF:magnification.MagSetColorEffect
title: MagSetColorEffect function
author: windows-sdk-content
description: Sets the color transformation matrix for a magnifier control.
old-location: magapi\magapi_MagSetColorEffect.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetcoloreffect.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MagSetColorEffect, MagSetColorEffect function [Magnification API], magapi.magapi_MagSetColorEffect, magapi_MagSetColorEffect, magnification/MagSetColorEffect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagSetColorEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagSetColorEffect function


## -description


Sets the color transformation matrix for a magnifier control.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pEffect [in]

Type: <b><a href="https://msdn.microsoft.com/eb7c283a-ea55-4e7c-8fd1-f106837ecc34">PMAGCOLOREFFECT</a></b>

The color transformation matrix, or <b>NULL</b> to remove the current color effect, if any.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The magnifier control uses the color transformation matrix to apply a color effect to the entire magnifier window. If the function is called multiple times, the most recent color transform is used.

This function requires Windows Display Driver Model (WDDM)-capable video cards.


#### Examples

The following example sets a color transformation matrix that converts the colors displayed in the magnifier to grayscale.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d86d3e43-5da0-460c-b243-d0797f5d0911">MagGetColorEffect</a>
 

 

