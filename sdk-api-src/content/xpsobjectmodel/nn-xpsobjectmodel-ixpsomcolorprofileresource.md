---
UID: NN:xpsobjectmodel.IXpsOMColorProfileResource
title: IXpsOMColorProfileResource (xpsobjectmodel.h)
description: Provides an IStream interface to a color profile resource.helpviewer_keywords: ["IXpsOMColorProfileResource","IXpsOMColorProfileResource interface [XPS Documents and Packaging]","IXpsOMColorProfileResource interface [XPS Documents and Packaging]","described","xps.ixpsomcolorprofileresource","xpsobjectmodel/IXpsOMColorProfileResource"]
old-location: xps\ixpsomcolorprofileresource.htm
tech.root: printdocs
ms.assetid: 8a344300-c3fc-4225-bfa5-d5d33798a094
ms.date: 12/05/2018
ms.keywords: IXpsOMColorProfileResource, IXpsOMColorProfileResource interface [XPS Documents and Packaging], IXpsOMColorProfileResource interface [XPS Documents and Packaging],described, xps.ixpsomcolorprofileresource, xpsobjectmodel/IXpsOMColorProfileResource
f1_keywords:
- xpsobjectmodel/IXpsOMColorProfileResource
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
- IXpsOMColorProfileResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMColorProfileResource interface


## -description


Provides an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to a color profile resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMColorProfileResource</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMColorProfileResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMColorProfileResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresource-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresource-setcontent">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMColorProfileResource    *newInterface;
IOpcPartUri                   *partUri;

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
    // The partUriString and acquiredStream variables 
    //   are defined outside of this example.
    hr = xpsFactory->CreatePartUri(
        partUriString, 
        &partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreateColorProfileResource (
            acquiredStream, 
            partUri,
            &newInterface);
        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface->Release();
        }
        partUri->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcolorprofileresource">IXpsOMObjectFactory::CreateColorProfileResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

