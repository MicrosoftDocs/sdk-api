---
UID: NF:xpsobjectmodel.IXpsOMPackageTarget.CreateXpsOMPackageWriter
title: IXpsOMPackageTarget::CreateXpsOMPackageWriter
author: windows-sdk-content
description: Create an IXpsOMPackageWriter interface for use with a print job that the StartXpsPrintJob1 function created.
old-location: xps\ixpsompackagetarget_createxpsompackagewriter.htm
tech.root: printdocs
ms.assetid: 6AD4BEB8-86B7-4085-9B84-D723982933FE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateXpsOMPackageWriter, CreateXpsOMPackageWriter method [XPS Documents and Packaging], CreateXpsOMPackageWriter method [XPS Documents and Packaging],IXpsOMPackageTarget interface, IXpsOMPackageTarget interface [XPS Documents and Packaging],CreateXpsOMPackageWriter method, IXpsOMPackageTarget.CreateXpsOMPackageWriter, IXpsOMPackageTarget::CreateXpsOMPackageWriter, xps.ixpsompackagetarget_createxpsompackagewriter, xpsobjectmodel/IXpsOMPackageTarget::CreateXpsOMPackageWriter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 with SP1, Windows Server 2008 and Platform Update Supplement for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: XpsPrint.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.lib
 - XpsPrint.dll
api_name:
 - IXpsOMPackageTarget.CreateXpsOMPackageWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageTarget::CreateXpsOMPackageWriter


## -description


Create an <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface for use with a print job that the  <a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a> function created.


## -parameters




### -param documentSequencePartName [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.


### -param documentSequencePrintTicket [in, optional]

The <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file. Set this parameter to <b>NULL</b> if you do not have a package-level print ticket.


### -param discardControlPartName [in, optional]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the name of the discard control part. Set this parameter to <b>NULL</b> if you do not have a discard control part.


### -param packageWriter [out, retval]

A pointer to the new  <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface that this method created.


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
<i>packageWriter</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>documentSequencePrintTicket</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/980D2A37-933F-41B1-A975-6BC797E8E770">IXpsOMPackageTarget</a>



<a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

