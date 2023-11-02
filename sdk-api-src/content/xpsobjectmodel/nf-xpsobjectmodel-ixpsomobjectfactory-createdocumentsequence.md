---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateDocumentSequence
title: IXpsOMObjectFactory::CreateDocumentSequence (xpsobjectmodel.h)
description: Creates an IXpsOMDocumentSequence interface, which can contain the IXpsOMDocument interfaces of the XPS document.
helpviewer_keywords: ["CreateDocumentSequence","CreateDocumentSequence method [XPS Documents and Packaging]","CreateDocumentSequence method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateDocumentSequence method","IXpsOMObjectFactory.CreateDocumentSequence","IXpsOMObjectFactory::CreateDocumentSequence","xps.ixpsomobjectfactory_createdocumentsequence","xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentSequence"]
old-location: xps\ixpsomobjectfactory_createdocumentsequence.htm
tech.root: xps
ms.assetid: 51d42b34-3380-4464-8feb-d03935f88077
ms.date: 12/05/2018
ms.keywords: CreateDocumentSequence, CreateDocumentSequence method [XPS Documents and Packaging], CreateDocumentSequence method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateDocumentSequence method, IXpsOMObjectFactory.CreateDocumentSequence, IXpsOMObjectFactory::CreateDocumentSequence, xps.ixpsomobjectfactory_createdocumentsequence, xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentSequence
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
 - IXpsOMObjectFactory::CreateDocumentSequence
 - xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentSequence
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
 - IXpsOMObjectFactory.CreateDocumentSequence
---

# IXpsOMObjectFactory::CreateDocumentSequence


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface, which  can contain the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interfaces of the XPS document.

## -parameters

### -param partUri [in]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource. This parameter must not be <b>NULL</b>.

### -param documentSequence [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a> interface.

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
<i>partUri</i> or <i>documentSequence</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMDocumentSequence    *newInterface;
IOpcPartUri               *partUri;

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
        hr = xpsFactory->CreateDocumentSequence (partUri, &newInterface);

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



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence">IXpsOMDocumentSequence</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>