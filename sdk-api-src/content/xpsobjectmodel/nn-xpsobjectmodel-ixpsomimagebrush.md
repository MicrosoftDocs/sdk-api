---
UID: NN:xpsobjectmodel.IXpsOMImageBrush
title: IXpsOMImageBrush
author: windows-sdk-content
description: A brush that uses a raster image as a source.
old-location: xps\ixpsomimagebrush.htm
old-project: printdocs
ms.assetid: f5478582-466b-496e-b7f3-42fb8caa6814
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMImageBrush, IXpsOMImageBrush interface [XPS Documents and Packaging], IXpsOMImageBrush interface [XPS Documents and Packaging],described, xps.ixpsomimagebrush, xpsobjectmodel/IXpsOMImageBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMImageBrush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageBrush interface


## -description


A brush that uses a raster image as a source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMImageBrush</b> interface inherits from <a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>. <b>IXpsOMImageBrush</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7c10f6e5-b223-4ddb-9fcf-c9f7bf82953f">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7472f84b-cd14-4b9f-8ea9-69e743319d05">GetColorProfileResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface, which  contains the color profile resource that is associated with the image.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92b03d98-22ce-4856-afe1-d13fb74eb340">GetImageResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface, which contains the image resource to be used as the source for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d18511b7-13ed-4528-9f3d-aef3bcadc403">SetColorProfileResource</a>
</td>
<td align="left" width="63%">
Sets a pointer to the <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface, which contains the color profile resource that is associated with the image.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c3c5189-0090-48c7-bc36-c9014758b968">SetImageResource</a>
</td>
<td align="left" width="63%">
Sets a pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the image resource to be used as the source for the brush.
            

</td>
</tr>
</table> 


## -remarks



The image used by this brush is defined in a coordinate space that is specified by the image's resolution. The image type must be JPEG, PNG, TIFF 6.0, or HD  Photo.

The code example that follows illustrates how to create an instance of  this interface.

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




<a href="https://msdn.microsoft.com/f271e152-8120-49c4-804d-069e224c6597">IXpsOMObjectFactory::CreateImageBrush</a>



<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

