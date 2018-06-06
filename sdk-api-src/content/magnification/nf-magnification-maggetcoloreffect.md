---
UID: NF:magnification.MagGetColorEffect
title: MagGetColorEffect function
author: windows-sdk-content
description: Gets the color transformation matrix for a magnifier control.
old-location: magapi\magapi_MagGetColorEffect.htm
old-project: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetcoloreffect.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: MagGetColorEffect, MagGetColorEffect function [Magnification API], magapi.magapi_MagGetColorEffect, magapi_MagGetColorEffect, magnification/MagGetColorEffect
ms.prod: windows
ms.technology: windows-sdk
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
 - MagGetColorEffect
product: Windows
targetos: Windows
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
---

# MagGetColorEffect function


## -description


 Gets the color transformation matrix for a magnifier control.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pEffect [out]

Type: <b><a href="https://msdn.microsoft.com/eb7c283a-ea55-4e7c-8fd1-f106837ecc34">PMAGCOLOREFFECT</a></b>

The color transformation matrix, or <b>NULL</b> if no color effect has been set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The magnifier control uses the color transformation matrix to apply a color effect to the entire magnifier window. 

This function requires Windows Display Driver Model (WDDM)-capable video cards.


#### Examples

The following example retrieves the color transformation matrix.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Retrieves the color transformation matrix from a magnifier control.
// Parameters:
//   hwndMag - handle of the magnifier control.
//
BOOL GetMagnifierColorTransform(HWND hwndMag)
{
    MAGCOLOREFFECT effect;

    BOOL ret = MagGetColorEffect(hwndMag, &amp;effect);

    //
    // Do something with the color data.
    //

    return ret;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/53749109-5370-45e7-ba90-79ad1504c41e">MagSetColorEffect</a>
 

 

