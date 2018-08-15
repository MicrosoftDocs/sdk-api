---
UID: NF:magnification.MagGetFullscreenColorEffect
title: MagGetFullscreenColorEffect function
author: windows-sdk-content
description: Retrieves the color transformation matrix associated with the full-screen magnifier.
old-location: magapi\magapi_maggetfullscreencoloreffect.htm
old-project: magapi
ms.assetid: 1C37DB20-1267-447B-A34F-E3EC83F51907
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MagGetFullscreenColorEffect, MagGetFullscreenColorEffect function [Magnification API], magapi.magapi_maggetfullscreencoloreffect, magnification/MagGetFullscreenColorEffect
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
 - MagGetFullscreenColorEffect
product: Windows
targetos: Windows
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
---

# MagGetFullscreenColorEffect function


## -description


Retrieves the color transformation matrix  associated with the  full-screen magnifier.


## -parameters




### -param pEffect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms692383(v=VS.85).aspx">PMAGCOLOREFFECT</a></b>

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
 

 

