---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

