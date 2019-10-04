---
UID: NN:xpsobjectmodel.IXpsOMImageBrush
title: IXpsOMImageBrush (xpsobjectmodel.h)
author: windows-sdk-content
description: A brush that uses a raster image as a source.
old-location: xps\ixpsomimagebrush.htm
tech.root: printdocs
ms.assetid: f5478582-466b-496e-b7f3-42fb8caa6814
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMImageBrush, IXpsOMImageBrush interface [XPS Documents and Packaging], IXpsOMImageBrush interface [XPS Documents and Packaging],described, xps.ixpsomimagebrush, xpsobjectmodel/IXpsOMImageBrush
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMImageBrush"
dev_langs:
 - c++
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
 - IXpsOMImageBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMImageBrush interface


## -description


A brush that uses a raster image as a source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMImageBrush</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>. <b>IXpsOMImageBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMImageBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomimagebrush-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomimagebrush-getcolorprofileresource">GetColorProfileResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface, which  contains the color profile resource that is associated with the image.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomimagebrush-getimageresource">GetImageResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface, which contains the image resource to be used as the source for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomimagebrush-setcolorprofileresource">SetColorProfileResource</a>
</td>
<td align="left" width="63%">
Sets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface, which contains the color profile resource that is associated with the image.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomimagebrush-setimageresource">SetImageResource</a>
</td>
<td align="left" width="63%">
Sets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface that contains the image resource to be used as the source for the brush.
            

</td>
</tr>
</table> 


## -remarks



The image used by this brush is defined in a coordinate space that is specified by the image's resolution. The image type must be JPEG, PNG, TIFF 6.0, or HD  Photo.

The code example that follows illustrates how to create an instance of  this interface.


```cpp

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
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreateImageBrush (
        image,
        &viewBox,
        &viewPort,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createimagebrush">IXpsOMObjectFactory::CreateImageBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

