---
UID: NF:d2d1.ID2D1BitmapBrush.SetExtendModeY
title: ID2D1BitmapBrush::SetExtendModeY
author: windows-sdk-content
description: Specifies how the brush vertically tiles those areas that extend past its bitmap.
old-location: direct2d\ID2D1BitmapBrush_SetExtendModeY.htm
tech.root: direct2d
ms.assetid: 6039ad41-e4b4-41e2-a4b1-31ad93ba88fd
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetExtendModeY method, ID2D1BitmapBrush.SetExtendModeY, ID2D1BitmapBrush::SetExtendModeY, SetExtendModeY, SetExtendModeY method [Direct2D], SetExtendModeY method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetExtendModeY, direct2d.ID2D1BitmapBrush_SetExtendModeY
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
 - ID2D1BitmapBrush.SetExtendModeY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapBrush::SetExtendModeY


## -description


Specifies how the brush vertically tiles those areas that extend past its bitmap.


## -parameters




### -param extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

A value that specifies how the brush vertically tiles those areas that extend past its bitmap.


## -returns



This method does not return a value.




## -remarks



Sometimes, the  bitmap for a bitmap brush doesn't completely fill the area being painted. When this happens, Direct2D uses the brush's horizontal (<a href="https://msdn.microsoft.com/bb20c9ea-a2b1-4fa5-a0e3-b788fe493993">SetExtendModeX</a>) and vertical (<b>SetExtendModeY</b>) extend mode settings to determine how to fill the remaining area.

The following illustration shows the results from  every  possible combination of the extend modes for an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>: <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE_CLAMP</a> (CLAMP), <b>D2D1_EXTEND_MODE_WRAP</b> (WRAP), and <b>D2D1_EXTEND_MIRROR</b> (MIRROR).

<img alt="Illustration of a bitmap and the resulting images from various extend modes" src="images/bitmapwrap_clamp_mirror.png"/>


#### Examples

The following example shows how to set the bitmap brush's x- and y-extend modes to <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MIRROR</a>. It  then paints the rectangle with the <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>.

It produces the following output.

<img alt="Illustration of an original image and the resulting image from setting both x- and y- extend modes to mirror" src="images/brushes_ovw_bitmapmirrormirror.png"/>

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>m_pBitmapBrush-&gt;SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush-&gt;SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget-&gt;FillRectangle(exampleRectangle, m_pBitmapBrush);
</pre>
</td>
</tr>
</table></span></div>
For more information about bitmap brushes, see the <a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>



<a href="https://msdn.microsoft.com/e71fef61-9d6a-441b-a88f-9f2cead23ecd">ID2D1BitmapBrush::GetExtendModeY</a>
 

 

