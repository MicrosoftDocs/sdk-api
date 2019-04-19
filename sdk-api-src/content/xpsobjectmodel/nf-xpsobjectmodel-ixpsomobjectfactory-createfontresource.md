---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateFontResource
title: IXpsOMObjectFactory::CreateFontResource (xpsobjectmodel.h)
author: windows-sdk-content
description: Creates an IXpsOMFontResource interface, which provides an IStream interface to the font resource.
old-location: xps\ixpsomobjectfactory_createfontresource.htm
tech.root: printdocs
ms.assetid: 9893716b-5004-4886-9bed-49a447e97f42
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFontResource, CreateFontResource method [XPS Documents and Packaging], CreateFontResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateFontResource method, IXpsOMObjectFactory.CreateFontResource, IXpsOMObjectFactory::CreateFontResource, TRUE, xps.ixpsomobjectfactory_createfontresource, xpsobjectmodel/IXpsOMObjectFactory::CreateFontResource
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
 - IXpsOMObjectFactory.CreateFontResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMObjectFactory::CreateFontResource


## -description


Creates an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface, which provides an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to the font resource.


## -parameters




### -param acquiredStream [in]

The read-only <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to be associated with this font resource. This parameter must not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>
<div class="alert"><b>Caution</b>  This stream is not to be obfuscated.</div>
<div> </div>

### -param fontEmbedding [in]

The <a href="https://msdn.microsoft.com/en-us/library/Dd372957(v=VS.85).aspx">XPS_FONT_EMBEDDING</a> value that specifies the stream's embedding option.


### -param partUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be assigned    to this resource. This parameter must not  be <b>NULL</b>.


### -param isObfSourceStream [in]

A Boolean value that indicates whether the stream referenced by <i>acquiredStream</i> is obfuscated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The stream referenced by <i>acquiredStream</i> is obfuscated.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The stream referenced by <i>acquiredStream</i> is  not obfuscated.

</td>
</tr>
</table>
 


### -param fontResource [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface.
          


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
One of the following errors  has occurred:

<ul>
<li><i>fontEmbedding</i> is not a  valid <a href="https://msdn.microsoft.com/en-us/library/Dd372957(v=VS.85).aspx">XPS_FONT_EMBEDDING</a> value.</li>
<li><i>fontEmbedding</i> is <a href="https://msdn.microsoft.com/en-us/library/Dd372957(v=VS.85).aspx">XPS_FONT_EMBEDDING_NORMAL</a> and  <i>isObfSourceStream</i> is <b>TRUE</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>acquiredStream</i>,  <i>partUri</i>, or <i>fontResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The value of <i>isObfSourceStream</i> describes the state of the <i>acquiredStream</i>-referenced stream  at  the time the font resource is created. All subsequent calls to <a href="https://msdn.microsoft.com/d512e862-e2d0-4cc8-a20a-bc3cfbfbcc47">GetStream</a> or <a href="https://msdn.microsoft.com/87a9d003-9406-4c94-b814-4986d213ee47">SetContent</a> will operate on unobfuscated versions of <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.

An error is returned if <i>isObfSourceStream</i> is set to <b>TRUE</b> and <i>fontEmbedding</i> is set to <a href="https://msdn.microsoft.com/en-us/library/Dd372957(v=VS.85).aspx">XPS_FONT_EMBEDDING_NORMAL</a>, or if the name referenced by <i>partUri</i> does not conform to the syntax for obfuscated streams.

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMFontResource    *newInterface;
IOpcPartUri           *partUri;

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
        hr = xpsFactory->CreateFontResource (
            acquiredStream, 
            XPS_FONT_EMBEDDING_NORMAL,    // normal
            partUri, 
            FALSE,                        // not obfuscated
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




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372957(v=VS.85).aspx">XPS_FONT_EMBEDDING</a>
 

 

