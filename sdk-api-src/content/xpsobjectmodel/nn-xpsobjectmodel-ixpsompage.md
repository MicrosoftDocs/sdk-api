---
UID: NN:xpsobjectmodel.IXpsOMPage
title: IXpsOMPage (xpsobjectmodel.h)
description: Provides the root node of a tree of objects that hold the contents of a single page.
helpviewer_keywords: ["IXpsOMPage","IXpsOMPage interface [XPS Documents and Packaging]","IXpsOMPage interface [XPS Documents and Packaging]","described","xps.ixpsompage","xpsobjectmodel/IXpsOMPage"]
old-location: xps\ixpsompage.htm
tech.root: xps
ms.assetid: 741deebd-9dce-4cd9-883e-4586c10a4609
ms.date: 12/05/2018
ms.keywords: IXpsOMPage, IXpsOMPage interface [XPS Documents and Packaging], IXpsOMPage interface [XPS Documents and Packaging],described, xps.ixpsompage, xpsobjectmodel/IXpsOMPage
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
 - IXpsOMPage
 - xpsobjectmodel/IXpsOMPage
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
 - IXpsOMPage
---

# IXpsOMPage interface

## -description

Provides the root node of a tree of objects that hold the contents of  a single page. 

The <b>IXpsOMPage</b> interface corresponds to the <b>FixedPage</b> element in XPS document markup.

## -inheritance

The <b>IXpsOMPage</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>. <b>IXpsOMPage</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPage        *newInterface;
// The following values are defined outside of 
// this example.
//  LPWSTR        language;
//  XPS_SIZE      pageDimensions;

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
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreatePage (
            &pageDimensions,
            language,
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


For information about using this interface in a program, see <a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a> and <a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dd316970(v=vs.85)">Create a Blank XPS OM</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpage">IXpsOMObjectFactory::CreatePage</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpagefromstream">IXpsOMObjectFactory::CreatePageFromStream</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="/previous-versions/windows/desktop/dd372917(v=vs.85)">Navigate the XPS OM</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
