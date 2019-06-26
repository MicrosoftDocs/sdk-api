---
UID: NN:xpsobjectmodel.IXpsOMPartResources
title: IXpsOMPartResources (xpsobjectmodel.h)
author: windows-sdk-content
description: Provides access to all shared, part-based resources of the XPS document.
old-location: xps\ixpsompartresources.htm
tech.root: printdocs
ms.assetid: 9f706f23-25a0-40ee-93f4-3d7ac98ad6ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPartResources, IXpsOMPartResources interface [XPS Documents and Packaging], IXpsOMPartResources interface [XPS Documents and Packaging],described, xps.ixpsompartresources, xpsobjectmodel/IXpsOMPartResources
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMPartResources"
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
 - IXpsOMPartResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPartResources interface


## -description


Provides access to all shared, part-based resources of the XPS document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPartResources</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPartResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPartResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompartresources-getcolorprofileresources">GetColorProfileResources</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection">IXpsOMColorProfileResourceCollection</a> interface that contains  the color profiles that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompartresources-getfontresources">GetFontResources</a>
</td>
<td align="left" width="63%">
Gets the   <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection">IXpsOMFontResourceCollection</a> interface that contains the fonts that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompartresources-getimageresources">GetImageResources</a>
</td>
<td align="left" width="63%">
Gets the  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection">IXpsOMImageResourceCollection</a> interface that contains the images that are used in the XPS document.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompartresources-getremotedictionaryresources">GetRemoteDictionaryResources</a>
</td>
<td align="left" width="63%">
Gets the  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection">IXpsOMRemoteDictionaryResourceCollection</a> interface that contains the remote resource dictionaries  that are used in the XPS document.
            

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPartResources    *newInterface;

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
    hr = xpsFactory->CreatePartResources (&newInterface);

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




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpartresources">IXpsOMObjectFactory::CreatePartResources</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

