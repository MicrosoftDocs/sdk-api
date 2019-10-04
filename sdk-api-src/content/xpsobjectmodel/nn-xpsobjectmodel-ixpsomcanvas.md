---
UID: NN:xpsobjectmodel.IXpsOMCanvas
title: IXpsOMCanvas (xpsobjectmodel.h)
author: windows-sdk-content
description: A group of visual elements and related properties.
old-location: xps\ixpsomcanvas.htm
tech.root: printdocs
ms.assetid: 3cb0e1b3-88a8-4724-a3c5-0df416294e62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas, IXpsOMCanvas interface [XPS Documents and Packaging], IXpsOMCanvas interface [XPS Documents and Packaging],described, xps.ixpsomcanvas, xpsobjectmodel/IXpsOMCanvas
ms.topic: interface
f1_keywords: 
 - "xpsobjectmodel/IXpsOMCanvas"
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
 - IXpsOMCanvas
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCanvas interface


## -description


A group of visual elements and related properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMCanvas</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>. <b>IXpsOMCanvas</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMCanvas</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getaccessibilitylongdescription">GetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Gets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getaccessibilityshortdescription">GetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Gets a short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionary">GetDictionary</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the dictionary associated with the canvas.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionarylocal">GetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the local, unshared dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getdictionaryresource">GetDictionaryResource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface of the remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getusealiasededgemode">GetUseAliasedEdgeMode</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that determines whether the edges of the objects in the canvas are to be rendered using the aliased edge mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals">GetVisuals</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection">IXpsOMVisualCollection</a> interface that contains a collection of the visual objects in the canvas.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setaccessibilitylongdescription">SetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Sets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setaccessibilityshortdescription">SetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Sets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionarylocal">SetDictionaryLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface pointer of the local, unshared dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setdictionaryresource">SetDictionaryResource</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface pointer of the remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-setusealiasededgemode">SetUseAliasedEdgeMode</a>
</td>
<td align="left" width="63%">
Sets the value that determines whether the edges of objects in this canvas will be rendered using the aliased edge mode.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMCanvas    *newInterface;

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
    hr = xpsFactory->CreateCanvas (&newInterface);
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




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcanvas">IXpsOMObjectFactory::CreateCanvas</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

