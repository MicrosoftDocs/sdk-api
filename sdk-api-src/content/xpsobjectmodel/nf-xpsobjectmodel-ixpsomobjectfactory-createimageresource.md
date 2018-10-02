---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateImageResource
title: IXpsOMObjectFactory::CreateImageResource
author: windows-sdk-content
description: Creates an IXpsOMImageResource interface, which is used to access an image resource stream.
old-location: xps\ixpsomobjectfactory_createimageresource.htm
tech.root: printdocs
ms.assetid: 267f6e3e-ed1d-4ce7-a554-a943ac3f469d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateImageResource, CreateImageResource method [XPS Documents and Packaging], CreateImageResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateImageResource method, IXpsOMObjectFactory.CreateImageResource, IXpsOMObjectFactory::CreateImageResource, xps.ixpsomobjectfactory_createimageresource, xpsobjectmodel/IXpsOMObjectFactory::CreateImageResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsOMObjectFactory.CreateImageResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateImageResource


## -description


Creates an <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface, which is used to access an image resource stream.


## -parameters




### -param acquiredStream [in]

The read-only stream to be associated with this resource. This parameter must 	not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param contentType [in]

The <a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a> value that describes the image type of the stream that is referenced by <i>acquiredStream</i>.


### -param partUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be assigned to this resource. This parameter must not be <b>NULL</b>.


### -param imageResource [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<i>contentType</i> was not a valid <a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a> value.

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    // The partUriString and acquiredStream variables 
    //   are defined outside of this example.
    hr = xpsFactory-&gt;CreatePartUri(partUriString, &amp;partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory-&gt;CreateImageResource (
            acquiredStream,
            contentType,
            partUri,
            &amp;newInterface);
        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface-&gt;Release();
        }
        partUri-&gt;Release();
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




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a>
 

 

