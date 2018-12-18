---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateImageBrush
title: IXpsOMObjectFactory::CreateImageBrush
author: windows-sdk-content
description: Creates an IXpsOMImageBrush interface.
old-location: xps\ixpsomobjectfactory_createimagebrush.htm
tech.root: printdocs
ms.assetid: f271e152-8120-49c4-804d-069e224c6597
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateImageBrush, CreateImageBrush method [XPS Documents and Packaging], CreateImageBrush method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateImageBrush method, IXpsOMObjectFactory.CreateImageBrush, IXpsOMObjectFactory::CreateImageBrush, xps.ixpsomobjectfactory_createimagebrush, xpsobjectmodel/IXpsOMObjectFactory::CreateImageBrush
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreateImageBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateImageBrush


## -description


Creates an <a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a> interface.


## -parameters




### -param image [in]

The  <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the image to be used as the source image of the brush.




### -param viewBox [in]

The <a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a> structure that defines the <i>viewbox</i>, which is the area  of the source image that is used by the brush.


### -param viewPort [in]

The <a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a> structure that defines the <i>viewport</i>, which is the area covered by the first    tile in the output area.


### -param imageBrush [out, retval]

A pointer to the new  <a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>  interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>image</i>, <i>viewBox</i>, <i>viewPort</i>, or <i>imageBrush</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
<i>viewBox</i> or <i>viewPort</i> contains a rectangle or value that is not valid.

</td>
</tr>
</table>
 




## -remarks



The brush's viewbox specifies the portion of a source image or visual to be used as the tile image.

The coordinates of the brush's viewbox are relative to the source content, such that  (0,0) specifies the upper-left corner of the source content. For images, dimensions specified by the brush's viewbox are expressed in the units of 1/96". The corresponding pixel coordinates in the source image are calculated as follows: 

In the illustration that follows, the image on the left is an example of a source image, and  that on the far right is the brush that results after selecting the viewbox. 

<img alt="An illustration that shows a viewbox example" src="../images/CreateBrush.png"/>
If the source image resolution is 96 by 96 dots per inch and image dimensions are 96 by 96 pixels, the values of fields in the <i>viewbox</i> parameter are as follows:

The preceding parameter values correspond to the  source image as follows:<dl>
<dd>SourceLeft = (96 × 48) / 96  = 48 pixels from the left side</dd>
<dd>SourceTop = (96 × 24) / 96 = 24 pixels from the top</dd>
<dd>SourceWidth = (96 × 24) / 96 = 24 pixels wide</dd>
<dd>SourceHeight = (96 × 48) / 96 = 48 pixels high</dd>
</dl>


An image brush is a tile brush that takes an image, or a part of it,  transforms the image to create a tile, places the resulting tile in the viewport  (the destination geometry of the tile in  the output area), and fills the output area  as described by the tile mode.

The <i>viewport</i> is the area covered by the first tile in the output area. The viewport image is repeated throughout the output area as described by the tile mode.

The next  illustration shows how an image brush is used to fill an output area.  From left to right, the original image is transformed to fill the viewport, then placed in the viewport area of the output area, and then tiled to fill the output area.

<img alt="A figure that shows how a tile brush fills a geometry" src="../images/tile_cherry.png"/>
The code example that follows illustrates how this method is used to create a new  interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMImageBrush            *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMImageResource     *image;
//  XPS_RECT                viewBox;
//  XPS_RECT                viewPort;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreateImageBrush (
        image,
        &amp;viewBox,
        &amp;viewPort,
        &amp;newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface-&gt;Release();
    }
    xpsFactory-&gt;Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a>
 

 

