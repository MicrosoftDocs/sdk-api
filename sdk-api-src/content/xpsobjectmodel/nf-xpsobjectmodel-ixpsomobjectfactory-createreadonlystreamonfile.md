---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateReadOnlyStreamOnFile
title: IXpsOMObjectFactory::CreateReadOnlyStreamOnFile
author: windows-sdk-content
description: Creates a read-only IStream over the specified file.
old-location: xps\ixpsomobjectfactory_createreadonlystreamonfile.htm
tech.root: printdocs
ms.assetid: 00df5162-6fcd-4df8-b7d4-614c14aca8b5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateReadOnlyStreamOnFile, CreateReadOnlyStreamOnFile method [XPS Documents and Packaging], CreateReadOnlyStreamOnFile method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateReadOnlyStreamOnFile method, IXpsOMObjectFactory.CreateReadOnlyStreamOnFile, IXpsOMObjectFactory::CreateReadOnlyStreamOnFile, xps.ixpsomobjectfactory_createreadonlystreamonfile, xpsobjectmodel/IXpsOMObjectFactory::CreateReadOnlyStreamOnFile
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
 - IXpsOMObjectFactory.CreateReadOnlyStreamOnFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateReadOnlyStreamOnFile


## -description


Creates a read-only <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> over the specified file.


## -parameters




### -param filename [in]

The name of the file to be opened.


### -param stream [out, retval]

A stream over the specified file.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>filename</i> or <i>stream</i> is <b>NULL</b>.

</td>
</tr>
</table>
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



<b>CreateReadOnlyStreamOnFile</b> is a wrapper method for <a href="https://msdn.microsoft.com/d41bb51d-127c-4b24-8c93-4224404e0b2d">IOpcFactory::CreateStreamOnFile</a>. It has the same effect as calling the following:


```cpp
    hr = opcFactory->CreateStreamOnFile (
        fileName,
        OPC_STREAM_IO_READ,
        NULL,
        FILE_ATTRIBUTE_NORMAL,
        &stream);

```





## -see-also




<a href="https://msdn.microsoft.com/d41bb51d-127c-4b24-8c93-4224404e0b2d">IOpcFactory::CreateStreamOnFile</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

