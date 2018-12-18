---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.AddPage
title: IXpsOMPackageWriter::AddPage
author: windows-sdk-content
description: Writes a new FixedPage part to the currently open FixedDocument part in the package.
old-location: xps\ixpsompackagewriter_addpage.htm
tech.root: printdocs
ms.assetid: d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddPage, AddPage method [XPS Documents and Packaging], AddPage method [XPS Documents and Packaging],IXpsOMPackageWriter interface, AddPage method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],AddPage method, IXpsOMPackageWriter.AddPage, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],AddPage method, IXpsOMPackageWriter3D::AddPage, IXpsOMPackageWriter::AddPage, xps.ixpsompackagewriter_addpage, xpsobjectmodel/IXpsOMPackageWriter3D::AddPage, xpsobjectmodel/IXpsOMPackageWriter::AddPage
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
 - IXpsOMPackageWriter.AddPage
 - IXpsOMPackageWriter3D.AddPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageWriter::AddPage


## -description


Writes a new FixedPage part to the currently open FixedDocument part in the package.


## -parameters




### -param page [in]

The <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface whose page content is to be written to the currently open FixedDocument of the  package.


### -param advisoryPageDimensions [in]

The <a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> structure that contains page dimensions.

Size is described in XPS units. There are 96 XPS units per inch.  For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.


### -param discardableResourceParts [in]

The <a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a> interface that contains a collection of the discardable resource parts.


### -param storyFragments [in]

The <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface that is to be  used for this page.


### -param pagePrintTicket [in]

The <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface that contains the page-level print ticket for this page. See also Remarks.


### -param pageThumbnail [in]

The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface that contains the thumbnail image of this page.


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
<dt><b>XPS_E_MISSING_DISCARDCONTROL</b></dt>
</dl>
</td>
<td width="60%">
A page refers to discardable resources but does not specify a DiscardControl part name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MISSING_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
This method was called before <a href="https://msdn.microsoft.com/da5fdbcd-ff3c-403a-a565-1590908cf333">StartNewDocument</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_UNAVAILABLE_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
A severe error occurred and the contents of the XPS OM might be unrecoverable. Some components of the XPS OM might still be usable but only after they have been verified. Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.

</td>
</tr>
</table>
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



Call this method  after calling <a href="https://msdn.microsoft.com/da5fdbcd-ff3c-403a-a565-1590908cf333">StartNewDocument</a>.

This method creates a new FixedPage  part in the package, copies the contents of the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that is passed in the <i>page</i> parameter, and then closes the new FixedPage  part after the page has been written to the package.

If <i>pagePrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_ON</b>,  this method creates a blank page-level print ticket, if one does not already exist. Each time method is called with a <b>NULL</b> pointer in <i>pagePrintTicket</i>, it adds a relationship from the new page to the blank print ticket. This is done to provide more efficient streaming consumption of the package.

If <i>pagePrintTicket</i> contains a <b>NULL</b> pointer and the package writer was created with interleaving set to <b>XPS_INTERLEAVING_OFF</b>,  no blank print ticket is created.




## -see-also




<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a>



<a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/eff1ab1e-2205-4f5c-9e32-199e073f5dbf">Using the IXpsOMPackageWriter Interface</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a>
 

 

