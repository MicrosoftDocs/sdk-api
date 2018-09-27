---
UID: NF:d2d1helper.ColorF.ColorF(Enum,FLOAT)
title: ColorF::ColorF(Enum,FLOAT)
author: windows-sdk-content
description: Instantiates a new instance of the ColorF class from the specified known color name and an alpha value.
old-location: direct2d\colorf_colorf_knowncolor__float_.htm
tech.root: Direct2D
ms.assetid: 08efc02c-7394-4e44-a704-fa4045d598c6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ColorF, ColorF interface [Direct2D],ColorF(Enum knownColor,FLOAT) constructor, ColorF(Enum knownColor,FLOAT) constructor [Direct2D], ColorF(Enum knownColor,FLOAT) constructor [Direct2D],ColorF interface, ColorF.ColorF, ColorF.ColorF(Enum,FLOAT), ColorF::ColorF, ColorF::ColorF(Enum knownColor,FLOAT), ColorF::ColorF(Enum knownColor,FLOAT)(Enum,FLOAT), ColorF::ColorF(Enum,FLOAT), D2D1.ColorF.ColorF(Enum knownColor,FLOAT), D2D1::ColorF::ColorF(Enum knownColor,FLOAT), d2d1helper/ColorF::ColorF(Enum knownColor,FLOAT), direct2d.colorf_colorf_knowncolor__float_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: D2D1
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
 - ColorF.ColorF(Enum knownColor, FLOAT)
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorF::ColorF(Enum,FLOAT)


## -description


Instantiates a new instance of the <a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a> class from the specified known color name and an alpha value.


## -parameters




### -param knownColor

Type: <b>Enum</b>

A constant value, defined by the <a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a> class,  that indicates a known color.  For example, D2D1::ColorF::Orange.


### -param a

Type: <b>FLOAT</b>

The alpha value for the color to be constructed. An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0  represents a fully opaque color. The default value is 1.0.


## -remarks



For a complete list of predefined colors, see the Color constants section of the  <a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a> class.  


#### Examples

The following example creates a predefined color and uses it to specify the color of an <a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a>. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>hr = m_pRenderTarget-&gt;CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &amp;m_pBlackBrush
    );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a>
 

 

