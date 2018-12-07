---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.AddResource
title: IXpsOMPackageWriter::AddResource
author: windows-sdk-content
description: Creates a new part resource in the package.
old-location: xps\ixpsompackagewriter_addresource.htm
tech.root: printdocs
ms.assetid: eb81efb8-f3cd-448d-ab60-34acf13db4cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddResource, AddResource method [XPS Documents and Packaging], AddResource method [XPS Documents and Packaging],IXpsOMPackageWriter interface, AddResource method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],AddResource method, IXpsOMPackageWriter.AddResource, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],AddResource method, IXpsOMPackageWriter3D::AddResource, IXpsOMPackageWriter::AddResource, xps.ixpsompackagewriter_addresource, xpsobjectmodel/IXpsOMPackageWriter3D::AddResource, xpsobjectmodel/IXpsOMPackageWriter::AddResource
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
 - IXpsOMPackageWriter.AddResource
 - IXpsOMPackageWriter3D.AddResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageWriter::AddResource


## -description


Creates a new part resource in the package.


## -parameters




### -param resource [in]

The <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a> interface of the part resource that will be added as a new part in the package. See Remarks for the types of resources that may be passed in this parameter.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A resource with the same name as the resource that is referenced by <i>resource</i> has already been added to the stream or there is no  relationship that includes the resource that is referenced by <i>resource</i>.

After <b>E_INVALIDARG</b> is returned, the stream or file is no longer valid and <a href="https://msdn.microsoft.com/916fbdaa-bef7-4a6f-9259-47347b47dc27">Close</a> will return  <b>XPS_E_UNAVAILABLE_PACKAGE</b>.

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



This method creates a new part in the document package that corresponds to <i>resource</i>, adds the contents of  <i>resource</i> to the new part, and then closes the new  part.

If this method returns an error, the package writer is no longer usable.

The <i>resource</i> parameter must be one of the following:<ul>
<li>The <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface of a font resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of an image resource that is used in the current page or  a page that has already been added.</li>
<li>The <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface of  color profile resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a> interface of a story fragments resource that is used in the current page or a page that has already been added.</li>
<li>The <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface of a document structure resource that is used in the current document or a document that has already been added.</li>
<li>The <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface of a signature block resource that is used in the current document or a document that has already been added.</li>
</ul>


This method returns an error if <i>resource</i> contains one of the following:<ul>
<li>The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface of a remote resource dictionary.</li>
<li>The <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of a print ticket.</li>
<li>The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of a thumbnail image.</li>
</ul>


This method returns an error when <i>resource</i> references a resource that has the same name as  a resource that  has already been added to the stream or for which there is no existing relationship.




## -see-also




<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/eff1ab1e-2205-4f5c-9e32-199e073f5dbf">Using the IXpsOMPackageWriter Interface</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

