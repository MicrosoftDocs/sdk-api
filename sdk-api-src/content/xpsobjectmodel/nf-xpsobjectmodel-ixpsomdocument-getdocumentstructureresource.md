---
UID: NF:xpsobjectmodel.IXpsOMDocument.GetDocumentStructureResource
title: IXpsOMDocument::GetDocumentStructureResource
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDocumentStructureResource interface of the resource that contains structural information about the document.
old-location: xps\ixpsomdocument_getdocumentstructureresource.htm
tech.root: printdocs
ms.assetid: 372aa8fd-efbb-4196-9137-4a9581c69f6c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDocumentStructureResource, GetDocumentStructureResource method [XPS Documents and Packaging], GetDocumentStructureResource method [XPS Documents and Packaging],IXpsOMDocument interface, IXpsOMDocument interface [XPS Documents and Packaging],GetDocumentStructureResource method, IXpsOMDocument.GetDocumentStructureResource, IXpsOMDocument::GetDocumentStructureResource, xps.ixpsomdocument_getdocumentstructureresource, xpsobjectmodel/IXpsOMDocument::GetDocumentStructureResource
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
 - IXpsOMDocument.GetDocumentStructureResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocument::GetDocumentStructureResource


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface of the resource that contains structural information about the document.


## -parameters




### -param documentStructureResource [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface of the resource. A <b>NULL</b> pointer is returned if an <b>IXpsOMDocumentStructureResource</b> interface is not present or has not been specified.


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
<i>documentStructureResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

