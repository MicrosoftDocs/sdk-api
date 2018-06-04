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

# IXpsOMPackageWriter3D interface


## -description


Contains methods that support model textures and print ticket.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackageWriter3D</b> interface inherits from <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>. <b>IXpsOMPackageWriter3D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackageWriter3D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76FC9938-914C-4328-BE71-DC898241D9EA">AddModelTexture</a>
</td>
<td align="left" width="63%">
Creates a new 3D model texture from the specified texture part and stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">IXpsOMPackageWriter::AddPage</a>
</td>
<td align="left" width="63%">
Writes a new FixedPage part to the currently open FixedDocument part in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb81efb8-f3cd-448d-ab60-34acf13db4cd">IXpsOMPackageWriter::AddResource</a>
</td>
<td align="left" width="63%">
Creates a new part resource in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/916fbdaa-bef7-4a6f-9259-47347b47dc27">IXpsOMPackageWriter::Close</a>
</td>
<td align="left" width="63%">
Closes any open parts of the package, then closes the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f782432-3d36-466c-b265-9da99d97565e">IXpsOMPackageWriter::IsClosed</a>
</td>
<td align="left" width="63%">
Gets the status of the <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da5fdbcd-ff3c-403a-a565-1590908cf333">IXpsOMPackageWriter::StartNewDocument</a>
</td>
<td align="left" width="63%">
Opens and initializes a new FixedDocument in the FixedDocumentSequence of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2CCA48A9-CB7C-40F9-8BE0-FEC74AA25902">SetModelPrintTicket</a>
</td>
<td align="left" width="63%">
Creates a print ticket with the specified part.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B8B43CE5-2222-428B-8E78-C7049D027EE1">IXpsDocumentPackageTarget</a>



<a href="https://msdn.microsoft.com/7273235D-EB74-4FB2-B471-FCFF71741BF6">IXpsDocumentPackageTarget3D</a>



<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/F5A13938-FC6A-4158-BC39-43F7ACF7D406">Supporting 3D printing</a>
 

 

