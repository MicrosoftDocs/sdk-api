---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateColorProfileResource
title: IXpsOMObjectFactory::CreateColorProfileResource (xpsobjectmodel.h)
description: Creates an IXpsOMColorProfileResource interface, which is used to access a color profile resource stream.
helpviewer_keywords: ["CreateColorProfileResource","CreateColorProfileResource method [XPS Documents and Packaging]","CreateColorProfileResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateColorProfileResource method","IXpsOMObjectFactory.CreateColorProfileResource","IXpsOMObjectFactory::CreateColorProfileResource","xps.ixpsomobjectfactory_createcolorprofileresource","xpsobjectmodel/IXpsOMObjectFactory::CreateColorProfileResource"]
old-location: xps\ixpsomobjectfactory_createcolorprofileresource.htm
tech.root: xps
ms.assetid: cb4d1b49-fda6-46c3-a72a-21affdb7e82e
ms.date: 12/05/2018
ms.keywords: CreateColorProfileResource, CreateColorProfileResource method [XPS Documents and Packaging], CreateColorProfileResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateColorProfileResource method, IXpsOMObjectFactory.CreateColorProfileResource, IXpsOMObjectFactory::CreateColorProfileResource, xps.ixpsomobjectfactory_createcolorprofileresource, xpsobjectmodel/IXpsOMObjectFactory::CreateColorProfileResource
f1_keywords:
- xpsobjectmodel/IXpsOMObjectFactory.CreateColorProfileResource
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
- IXpsOMObjectFactory.CreateColorProfileResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMObjectFactory::CreateColorProfileResource


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface,  which is used to access a color profile resource stream.


## -parameters




### -param acquiredStream [in]

The read-only <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to be associated with this resource. This parameter must not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object;   do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.


### -param colorProfileResource [out, retval]

A pointer to the new <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>acquiredStream</i>, <i>partUri</i>, or <i>colorProfileResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The code example that follows illustrates how this method is used to create a new  interface.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

