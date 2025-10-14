---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateFontResource
title: IXpsOMObjectFactory::CreateFontResource (xpsobjectmodel.h)
description: Creates an IXpsOMFontResource interface, which provides an IStream interface to the font resource.
helpviewer_keywords: ["CreateFontResource","CreateFontResource method [XPS Documents and Packaging]","CreateFontResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","FALSE","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateFontResource method","IXpsOMObjectFactory.CreateFontResource","IXpsOMObjectFactory::CreateFontResource","TRUE","xps.ixpsomobjectfactory_createfontresource","xpsobjectmodel/IXpsOMObjectFactory::CreateFontResource"]
old-location: xps\ixpsomobjectfactory_createfontresource.htm
tech.root: xps
ms.assetid: 9893716b-5004-4886-9bed-49a447e97f42
ms.date: 12/05/2018
ms.keywords: CreateFontResource, CreateFontResource method [XPS Documents and Packaging], CreateFontResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, FALSE, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateFontResource method, IXpsOMObjectFactory.CreateFontResource, IXpsOMObjectFactory::CreateFontResource, TRUE, xps.ixpsomobjectfactory_createfontresource, xpsobjectmodel/IXpsOMObjectFactory::CreateFontResource
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
 - IXpsOMObjectFactory::CreateFontResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreateFontResource
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
 - IXpsOMObjectFactory.CreateFontResource
---

# IXpsOMObjectFactory::CreateFontResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface, which provides an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to the font resource.

## -parameters

### -param acquiredStream [in]

The read-only <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to be associated with this font resource. This parameter must not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>
<div class="alert"><b>Caution</b>  This stream is not to be obfuscated.</div>
<div> </div>

### -param fontEmbedding [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a> value that specifies the stream's embedding option.

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned    to this resource. This parameter must not  be <b>NULL</b>.

### -param isObfSourceStream [in]

A Boolean value that indicates whether the stream referenced by <i>acquiredStream</i> is obfuscated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The stream referenced by <i>acquiredStream</i> is obfuscated.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The stream referenced by <i>acquiredStream</i> is  not obfuscated.

</td>
</tr>
</table>

### -param fontResource [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface.

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
One of the following errors  has occurred:

<ul>
<li><i>fontEmbedding</i> is not a  valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a> value.</li>
<li><i>fontEmbedding</i> is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_NORMAL</a> and  <i>isObfSourceStream</i> is <b>TRUE</b>.</li>
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

The value of <i>isObfSourceStream</i> describes the state of the <i>acquiredStream</i>-referenced stream  at  the time the font resource is created. All subsequent calls to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomfontresource-getstream">GetStream</a> or <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomfontresource-setcontent">SetContent</a> will operate on unobfuscated versions of <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

An error is returned if <i>isObfSourceStream</i> is set to <b>TRUE</b> and <i>fontEmbedding</i> is set to <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_NORMAL</a>, or if the name referenced by <i>partUri</i> does not conform to the syntax for obfuscated streams.

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

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING</a>