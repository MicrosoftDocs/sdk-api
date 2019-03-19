---
UID: NF:magnification.MagGetInputTransform
title: MagGetInputTransform function (magnification.h)
author: windows-sdk-content
description: Retrieves the current input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.
old-location: magapi\magapi_maggetinputtransform.htm
tech.root: magapi
ms.assetid: 3825B5DB-BD25-4073-8EB3-65A57709A804
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MagGetInputTransform, MagGetInputTransform function [Magnification API], magapi.magapi_maggetinputtransform, magnification/MagGetInputTransform
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
 - MagGetInputTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagGetInputTransform function


## -description


Retrieves the current input transformation for pen and touch input, represented as a source rectangle and a destination rectangle.


## -parameters




### -param pfEnabled [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

TRUE  if input translation is enabled, or FALSE if not.


### -param pRectSource [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

The source rectangle, in unmagnified screen coordinates,  that defines the area of the screen that is magnified. 


### -param pRectDest [out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

The destination rectangle, in screen coordinates, that defines the area of the screen where the magnified screen content is displayed. Pen and touch input in this rectangle is mapped to the source rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



The input transformation maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space. This enables the system to pass touch and pen input that is entered in magnified screen content, to the correct UI element on the screen. For example, without input transformation, input is passed to the element located at the unmagnified screen coordinates, not to the item that appears in the magnified screen content. 


#### Examples

The following example retrieves the current input translation settings.


```cpp
// Description:
//   Retrieves the current input transform.
//
BOOL GetInputTranform()
{
    BOOL fInputTransformEnabled;
    RECT rcSource;
    RECT rcTarget;

    BOOL fResult = MagGetInputTransform(&fInputTransformEnabled, 
                                        &rcSource, &rcTarget);
    if (fResult)
    {
        //
        // Do something with the input transform data.
        //
    }

    return fResult;
}

```





## -see-also




<a href="https://msdn.microsoft.com/B42B59DB-9E21-4769-B605-014173514AEB">MagSetInputTransform</a>
 

 

