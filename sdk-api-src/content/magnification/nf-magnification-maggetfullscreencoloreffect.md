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

# MagGetFullscreenColorEffect function


## -description


Retrieves the color transformation matrix  associated with the  full-screen magnifier.


## -parameters




### -param pEffect [out]

Type: <b><a href="https://msdn.microsoft.com/eb7c283a-ea55-4e7c-8fd1-f106837ecc34">PMAGCOLOREFFECT</a></b>

The color transformation matrix, or the identity matrix if no color effect has been set. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The full-screen magnifier uses the color transformation matrix to apply a color effect to the entire screen.


#### Examples

The following example retrieves the color transformation matrix associated with the full-screen magnifier.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>        // Get the current color effect.
        MAGCOLOREFFECT magEffect;

        if (!MagGetFullscreenColorEffect(&amp;magEffect))
            return E_FAIL;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/F6CE5453-E427-46E4-81E8-6E96BA28C05C">MagSetFullscreenColorEffect</a>
 

 

