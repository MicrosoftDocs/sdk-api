---
UID: NN:xpsobjectmodel.IXpsOMPageReference
title: IXpsOMPageReference (xpsobjectmodel.h)
description: Enables virtualization of pages in an XPS document.
helpviewer_keywords: ["IXpsOMPageReference","IXpsOMPageReference interface [XPS Documents and Packaging]","IXpsOMPageReference interface [XPS Documents and Packaging]","described","xps.ixpsompagereference","xpsobjectmodel/IXpsOMPageReference"]
old-location: xps\ixpsompagereference.htm
tech.root: xps
ms.assetid: cdebab24-f918-4235-b4d5-5ee1007ade87
ms.date: 12/05/2018
ms.keywords: IXpsOMPageReference, IXpsOMPageReference interface [XPS Documents and Packaging], IXpsOMPageReference interface [XPS Documents and Packaging],described, xps.ixpsompagereference, xpsobjectmodel/IXpsOMPageReference
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPageReference
 - xpsobjectmodel/IXpsOMPageReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPageReference
---

# IXpsOMPageReference interface

## -description

Enables virtualization of pages in an XPS document.

A page reference defers loading of the full object model of a page until  the page is requested. If the page has not been altered, it  can also be unloaded on request.

## -inheritance

The <b>IXpsOMPageReference</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPageReference</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPageReference    *newInterface;
// The following value is defined outside of 
// this example.
XPS_SIZE        advisoryPageDimensions;

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
    hr = xpsFactory->CreatePageReference (
        &advisoryPageDimensions,
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


For information about using this interface in a program, see <a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a> and <a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource">IXpsOMDocumentStructureResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection">IXpsOMNameCollection</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpagereference">IXpsOMObjectFactory::CreatePageReference</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource">IXpsOMStoryFragmentsResource</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
