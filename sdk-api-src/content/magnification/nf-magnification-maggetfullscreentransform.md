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

# MagGetFullscreenTransform function


## -description


Retrieves the magnification settings for the full-screen magnifier.


## -parameters




### -param pMagLevel [out]

Type: <b>float*</b>

The current magnification factor for the full-screen magnifier.  A value of 1.0 indicates that the screen content is not being magnified. A value above 1.0 indicates the scale factor for magnification. A value less than 1.0 is not valid. 



### -param pxOffset [out]

Type: <b>int*</b>

The x-coordinate offset for the upper-left corner of the unmagnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates.


### -param pyOffset [out]

Type: <b>int*</b>

The y-coordinate offset for the upper-left corner of the unmagnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The offsets are not affected by the current dots per inch (dpi) setting.


#### Examples

The following code snippet retrieves the magnification value and offsets for the full-screen magnifier.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // Get the current magnification level and offset.
    float  magLevel;
    int    xOffset, yOffset;

    if (!MagGetFullscreenTransform(&amp;magLevel, &amp;xOffset, &amp;yOffset))
    {
        return E_FAIL;
    }
    
    // 
    // Do something with the magnification settings.
    //    
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/B02C2A37-6BA6-4DF8-92C1-748BF7B25B96">MagSetFullscreenTransform</a>
 

 

