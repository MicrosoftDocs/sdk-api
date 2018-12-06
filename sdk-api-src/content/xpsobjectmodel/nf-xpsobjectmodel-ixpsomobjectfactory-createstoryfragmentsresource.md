---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateStoryFragmentsResource
title: IXpsOMObjectFactory::CreateStoryFragmentsResource
author: windows-sdk-content
description: Creates an IXpsOMStoryFragmentsResource interface that provides access to the content of the resource stream of a page's StoryFragments part.
old-location: xps\ixpsomobjectfactory_createstoryfragmentsresource.htm
tech.root: printdocs
ms.assetid: b0e3f538-4af9-4d86-8899-6ea4e601eaad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateStoryFragmentsResource, CreateStoryFragmentsResource method [XPS Documents and Packaging], CreateStoryFragmentsResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateStoryFragmentsResource method, IXpsOMObjectFactory.CreateStoryFragmentsResource, IXpsOMObjectFactory::CreateStoryFragmentsResource, xps.ixpsomobjectfactory_createstoryfragmentsresource, xpsobjectmodel/IXpsOMObjectFactory::CreateStoryFragmentsResource
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
 - IXpsOMObjectFactory.CreateStoryFragmentsResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateStoryFragmentsResource


## -description


Creates an <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface that provides access to the content of the resource stream of a page's StoryFragments part.


## -parameters




### -param acquiredStream [in]

The read-only <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to be associated with this StoryFragments  resource.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name to be assigned to  this resource.


### -param storyFragmentsResource [out, retval]

A pointer to the new  <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface.
          


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
<i>acquiredStream</i>,  <i>partUri</i>, or <i>storyFragmentsResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The StoryFragments part of a page contains the XML markup that describes the structure of the portions of one or more stories  that are associated with a single fixed page. Some of the document contents that might be described by the XML markup in a StoryFragments part include  the story's tables and paragraphs that are found on the page.

The XML markup in  the DocumentStructure and StoryFragments parts is described in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

