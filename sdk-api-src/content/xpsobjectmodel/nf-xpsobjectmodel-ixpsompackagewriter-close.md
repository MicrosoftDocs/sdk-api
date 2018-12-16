---
UID: NF:xpsobjectmodel.IXpsOMPackageWriter.Close
title: IXpsOMPackageWriter::Close
author: windows-sdk-content
description: Closes any open parts of the package, then closes the package.
old-location: xps\ixpsompackagewriter_close.htm
tech.root: printdocs
ms.assetid: 916fbdaa-bef7-4a6f-9259-47347b47dc27
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Close, Close method [XPS Documents and Packaging], Close method [XPS Documents and Packaging],IXpsOMPackageWriter interface, Close method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, IXpsOMPackageWriter interface [XPS Documents and Packaging],Close method, IXpsOMPackageWriter.Close, IXpsOMPackageWriter3D interface [XPS Documents and Packaging],Close method, IXpsOMPackageWriter3D::Close, IXpsOMPackageWriter::Close, xps.ixpsompackagewriter_close, xpsobjectmodel/IXpsOMPackageWriter3D::Close, xpsobjectmodel/IXpsOMPackageWriter::Close
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
 - IXpsOMPackageWriter.Close
 - IXpsOMPackageWriter3D.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageWriter::Close


## -description


Closes any open parts of the package, then closes the package.


## -parameters






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



If any discardable parts that are referenced by a call to <a href="https://msdn.microsoft.com/d7ea638d-f95c-4d72-8f55-cbb6a7d1ae8d">AddPage</a> have not been received, an error will be returned.

After this method is called, calling any other <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> method except  <a href="https://msdn.microsoft.com/7f782432-3d36-466c-b265-9da99d97565e">IsClosed</a> will return an error.




## -see-also




<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/eff1ab1e-2205-4f5c-9e32-199e073f5dbf">Using the IXpsOMPackageWriter Interface</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

