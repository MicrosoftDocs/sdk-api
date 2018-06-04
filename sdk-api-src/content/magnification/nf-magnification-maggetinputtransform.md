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

# MagGetInputTransform function


## -description


Retrieves the current input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.


## -parameters




### -param pfEnabled [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

TRUE  if input translation is enabled, or FALSE if not.


### -param pRectSource

TBD


### -param pRectDest

TBD




#### - prcDest [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

The destination rectangle, in screen coordinates, that defines the area of the screen where the magnified screen content is displayed. Pen and touch input in this rectangle is mapped to the source rectangle.


#### - prcSource [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

The source rectangle, in unmagnified screen coordinates,  that defines the area of the screen that is magnified. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The input transformation maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space. This enables the system to pass touch and pen input that is entered in magnified screen content, to the correct UI element on the screen. For example, without input transformation, input is passed to the element located at the unmagnified screen coordinates, not to the item that appears in the magnified screen content. 


#### Examples

The following example retrieves the current input translation settings.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Retrieves the current input transform.
//
BOOL GetInputTranform()
{
    BOOL fInputTransformEnabled;
    RECT rcSource;
    RECT rcTarget;

    BOOL fResult = MagGetInputTransform(&amp;fInputTransformEnabled, 
                                        &amp;rcSource, &amp;rcTarget);
    if (fResult)
    {
        //
        // Do something with the input transform data.
        //
    }

    return fResult;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/B42B59DB-9E21-4769-B605-014173514AEB">MagSetInputTransform</a>
 

 

