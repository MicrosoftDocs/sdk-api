---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateImageResource
title: IXpsOMObjectFactory::CreateImageResource (xpsobjectmodel.h)
description: Creates an IXpsOMImageResource interface, which is used to access an image resource stream.
helpviewer_keywords: ["CreateImageResource","CreateImageResource method [XPS Documents and Packaging]","CreateImageResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateImageResource method","IXpsOMObjectFactory.CreateImageResource","IXpsOMObjectFactory::CreateImageResource","xps.ixpsomobjectfactory_createimageresource","xpsobjectmodel/IXpsOMObjectFactory::CreateImageResource"]
old-location: xps\ixpsomobjectfactory_createimageresource.htm
tech.root: xps
ms.assetid: 267f6e3e-ed1d-4ce7-a554-a943ac3f469d
ms.date: 12/05/2018
ms.keywords: CreateImageResource, CreateImageResource method [XPS Documents and Packaging], CreateImageResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateImageResource method, IXpsOMObjectFactory.CreateImageResource, IXpsOMObjectFactory::CreateImageResource, xps.ixpsomobjectfactory_createimageresource, xpsobjectmodel/IXpsOMObjectFactory::CreateImageResource
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
 - IXpsOMObjectFactory::CreateImageResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateImageResource
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
 - IXpsOMObjectFactory.CreateImageResource
---

# IXpsOMObjectFactory::CreateImageResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface, which is used to access an image resource stream.

## -parameters

### -param acquiredStream [in]

The read-only stream to be associated with this resource. This parameter must 	not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param contentType [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a> value that describes the image type of the stream that is referenced by <i>acquiredStream</i>.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource. This parameter must not be <b>NULL</b>.

### -param imageResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a> interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>contentType</i> was not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a> value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>acquiredStream</i>, <i>partUri</i>, or <i>imageResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMImageResource    *newInterface;
// The following values are defined outside of 
// this example.
//  IStream            *acquiredStream;
//  XPS_IMAGE_TYPE     contentType;
//  IOpcPartUri        *partUri;
    
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
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreateImageResource (
            acquiredStream,
            contentType,
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

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a>