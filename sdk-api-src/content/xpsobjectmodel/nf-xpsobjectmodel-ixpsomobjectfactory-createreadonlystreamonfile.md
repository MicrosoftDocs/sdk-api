---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateReadOnlyStreamOnFile
title: IXpsOMObjectFactory::CreateReadOnlyStreamOnFile (xpsobjectmodel.h)
description: Creates a read-only IStream over the specified file.
helpviewer_keywords: ["CreateReadOnlyStreamOnFile","CreateReadOnlyStreamOnFile method [XPS Documents and Packaging]","CreateReadOnlyStreamOnFile method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateReadOnlyStreamOnFile method","IXpsOMObjectFactory.CreateReadOnlyStreamOnFile","IXpsOMObjectFactory::CreateReadOnlyStreamOnFile","xps.ixpsomobjectfactory_createreadonlystreamonfile","xpsobjectmodel/IXpsOMObjectFactory::CreateReadOnlyStreamOnFile"]
old-location: xps\ixpsomobjectfactory_createreadonlystreamonfile.htm
tech.root: xps
ms.assetid: 00df5162-6fcd-4df8-b7d4-614c14aca8b5
ms.date: 12/05/2018
ms.keywords: CreateReadOnlyStreamOnFile, CreateReadOnlyStreamOnFile method [XPS Documents and Packaging], CreateReadOnlyStreamOnFile method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateReadOnlyStreamOnFile method, IXpsOMObjectFactory.CreateReadOnlyStreamOnFile, IXpsOMObjectFactory::CreateReadOnlyStreamOnFile, xps.ixpsomobjectfactory_createreadonlystreamonfile, xpsobjectmodel/IXpsOMObjectFactory::CreateReadOnlyStreamOnFile
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
 - IXpsOMObjectFactory::CreateReadOnlyStreamOnFile
 - xpsobjectmodel/IXpsOMObjectFactory::CreateReadOnlyStreamOnFile
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
 - IXpsOMObjectFactory.CreateReadOnlyStreamOnFile
---

# IXpsOMObjectFactory::CreateReadOnlyStreamOnFile


## -description

Creates a read-only <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> over the specified file.

## -parameters

### -param filename [in]

The name of the file to be opened.

### -param stream [out, retval]

A stream over the specified file.

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
<i>filename</i> or <i>stream</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

<b>CreateReadOnlyStreamOnFile</b> is a wrapper method for <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createstreamonfile">IOpcFactory::CreateStreamOnFile</a>. It has the same effect as calling the following:


```cpp
    hr = opcFactory->CreateStreamOnFile (
        fileName,
        OPC_STREAM_IO_READ,
        NULL,
        FILE_ATTRIBUTE_NORMAL,
        &stream);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createstreamonfile">IOpcFactory::CreateStreamOnFile</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>