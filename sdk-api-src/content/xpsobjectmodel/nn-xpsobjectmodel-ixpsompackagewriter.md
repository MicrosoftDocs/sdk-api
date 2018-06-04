---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IXpsOMPackageWriter interface


## -description


Incrementally writes the parts of an XPS document to  a package file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackageWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPackageWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackageWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">AddPage</a>
</td>
<td align="left" width="63%">
Writes a new FixedPage part to the currently open FixedDocument part in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb81efb8-f3cd-448d-ab60-34acf13db4cd">AddResource</a>
</td>
<td align="left" width="63%">
Creates a new part resource in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes any open parts of the package, then closes the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f782432-3d36-466c-b265-9da99d97565e">IsClosed</a>
</td>
<td align="left" width="63%">

              Gets the status of the <b>IXpsOMPackageWriter</b> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da5fdbcd-ff3c-403a-a565-1590908cf333">StartNewDocument</a>
</td>
<td align="left" width="63%">

              Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.
            

</td>
</tr>
</table> 


## -remarks



Progressive writing enables an application to serialize  XPS document content and resources as they become available. It does not require the application to create all elements of the document before serialization.

This interface writes the pages to the package sequentially, in the order that  <a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">AddPage</a> is called. The interface does not support page writing in a non-sequential order; thus it should only be used when page content is produced or is available for writing in the order it is to appear in the XPS document.




## -see-also




<a href="https://msdn.microsoft.com/D20AE05F-466F-44B6-972A-06AA872FF7BA">IXpsDocumentPackageTarget::GetXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/67d081a6-ec10-4cd3-8f77-b7653aef27a1">IXpsOMObjectFactory::CreatePackageWriterOnFile</a>



<a href="https://msdn.microsoft.com/77f432e3-7b6a-426f-8673-06dbf3038443">IXpsOMObjectFactory::CreatePackageWriterOnStream</a>



<a href="https://msdn.microsoft.com/eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b">Print an XPS OM</a>



<a href="https://msdn.microsoft.com/eff1ab1e-2205-4f5c-9e32-199e073f5dbf">Using the IXpsOMPackageWriter Interface</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

