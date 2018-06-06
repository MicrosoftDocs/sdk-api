---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateDocumentStructureResource
title: IXpsOMObjectFactory::CreateDocumentStructureResource
author: windows-sdk-content
description: Creates an IXpsOMDocumentStructureResource interface, which provides access to the document structure resource stream.
old-location: xps\ixpsomobjectfactory_createdocumentstructureresource.htm
old-project: printdocs
ms.assetid: ce41c5fb-033d-4140-b7aa-4f28676f0ae6
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CreateDocumentStructureResource, CreateDocumentStructureResource method [XPS Documents and Packaging], CreateDocumentStructureResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateDocumentStructureResource method, IXpsOMObjectFactory.CreateDocumentStructureResource, IXpsOMObjectFactory::CreateDocumentStructureResource, xps.ixpsomobjectfactory_createdocumentstructureresource, xpsobjectmodel/IXpsOMObjectFactory::CreateDocumentStructureResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreateDocumentStructureResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreateDocumentStructureResource


## -description


Creates an <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface, which provides access to the document structure resource stream.


## -parameters




### -param acquiredStream [in]


            The read-only <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>   interface to be associated with this resource. This parameter must not be <b>NULL</b>.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be assigned to this resource. This parameter must not be <b>NULL</b>.


### -param documentStructureResource [out, retval]


            A pointer to the new <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface.


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
<i>acquiredStream</i>,  <i>partUri</i>, or <i>documentStructureResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The DocumentStructure part of an XPS document contains the document outline, which, with the StoryFragments parts, defines the reading order of every element that appears in the fixed pages of the document. This interface enables a program to read the XML contents of the DocumentStructure  part and also to replace the XML contents of the DocumentStructure part.

The DocumentStructure part contains the document framework and the outline that describes the overall reading order of the document. The reading order is organized into semantic blocks called stories. Stories are logical units of the document in the same way as  articles are units in a magazine. Stories are made up of one or more StoryFragments parts.

The  StoryFragments parts contain content structure markup that defines the story's semantic blocks, such as the  paragraphs and tables that make up the story's content.

The content of the DocumentStructure and StoryFragments parts is described in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

