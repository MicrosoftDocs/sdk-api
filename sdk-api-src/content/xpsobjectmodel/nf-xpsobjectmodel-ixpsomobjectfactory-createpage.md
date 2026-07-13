---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePage
title: IXpsOMObjectFactory::CreatePage (xpsobjectmodel.h)
description: Creates an IXpsOMPage interface, which provides the root node of a tree of objects that represent the contents of a single page.
helpviewer_keywords: ["CreatePage","CreatePage method [XPS Documents and Packaging]","CreatePage method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePage method","IXpsOMObjectFactory.CreatePage","IXpsOMObjectFactory::CreatePage","xps.ixpsomobjectfactory_createpage","xpsobjectmodel/IXpsOMObjectFactory::CreatePage"]
old-location: xps\ixpsomobjectfactory_createpage.htm
tech.root: xps
ms.assetid: 9212ccd8-0793-40cc-bab5-609ea74715f7
ms.date: 12/05/2018
ms.keywords: CreatePage, CreatePage method [XPS Documents and Packaging], CreatePage method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePage method, IXpsOMObjectFactory.CreatePage, IXpsOMObjectFactory::CreatePage, xps.ixpsomobjectfactory_createpage, xpsobjectmodel/IXpsOMObjectFactory::CreatePage
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
 - IXpsOMObjectFactory::CreatePage
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePage
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
 - IXpsOMObjectFactory.CreatePage
---

# IXpsOMObjectFactory::CreatePage


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface,  which provides the root node of a tree of objects  that represent the contents of a single page.

## -parameters

### -param pageDimensions [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size">XPS_SIZE</a> structure that specifies the size of the page to be created.
          

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.

### -param language [in]

The string that indicates the default language of the created page.

<div class="alert"><b>Important</b>  The language string must follow the RFC 3066 syntax.</div>
<div> </div>

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.

### -param page [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>pageDimensions</i>, <i>partUri</i>, or   <i>page</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
<i>language</i> does not contain a valid language string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_PAGE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
<i>pageDimensions</i> contains an invalid page size or invalid page size values.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


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

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="http://tools.ietf.org/html/rfc3066">The Internet Engineering Task Force (IETF) RFC 3066</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>