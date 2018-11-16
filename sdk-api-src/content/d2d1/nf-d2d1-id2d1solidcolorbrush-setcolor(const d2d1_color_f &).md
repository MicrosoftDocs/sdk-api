---
UID: NF:d2d1.ID2D1SolidColorBrush.SetColor(const D2D1_COLOR_F &)
title: ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &)
author: windows-sdk-content
description: Specifies the color of this solid-color brush.
old-location: direct2d\ID2D1SolidColorBrush_SetColor_ref_COLOR_F.htm
tech.root: Direct2D
ms.assetid: f11d3528-e444-4a55-b522-0dad6ddcd735
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1SolidColorBrush interface [Direct2D],SetColor method, ID2D1SolidColorBrush.SetColor, ID2D1SolidColorBrush.SetColor(const D2D1_COLOR_F &), ID2D1SolidColorBrush::SetColor, ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &), SetColor, SetColor method [Direct2D], SetColor method [Direct2D],ID2D1SolidColorBrush interface, d2d1/ID2D1SolidColorBrush::SetColor, direct2d.ID2D1SolidColorBrush_SetColor_ref_COLOR_F
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SolidColorBrush.SetColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1SolidColorBrush.SetColor
: 
---

# ID2D1SolidColorBrush::SetColor(const D2D1_COLOR_F &)


## -description


Specifies the color of this solid-color brush.


## -parameters




### -param color [ref]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The color of this solid-color brush.


## -returns



This method does not return a value.




## -remarks



To help create colors, Direct2D provides the <a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a> class. It offers several helper methods for creating colors and provides a set or predefined colors. 


#### Examples

The following code shows  how to use this method.


```cpp
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );

```





## -see-also




<a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a>
 

 

