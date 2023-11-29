---
UID: NF:xpsobjectmodel.IXpsOMPackageTarget.CreateXpsOMPackageWriter
title: IXpsOMPackageTarget::CreateXpsOMPackageWriter (xpsobjectmodel.h)
description: Create an IXpsOMPackageWriter interface for use with a print job that the StartXpsPrintJob1 function created.
helpviewer_keywords: ["CreateXpsOMPackageWriter","CreateXpsOMPackageWriter method [XPS Documents and Packaging]","CreateXpsOMPackageWriter method [XPS Documents and Packaging]","IXpsOMPackageTarget interface","IXpsOMPackageTarget interface [XPS Documents and Packaging]","CreateXpsOMPackageWriter method","IXpsOMPackageTarget.CreateXpsOMPackageWriter","IXpsOMPackageTarget::CreateXpsOMPackageWriter","xps.ixpsompackagetarget_createxpsompackagewriter","xpsobjectmodel/IXpsOMPackageTarget::CreateXpsOMPackageWriter"]
old-location: xps\ixpsompackagetarget_createxpsompackagewriter.htm
tech.root: xps
ms.assetid: 6AD4BEB8-86B7-4085-9B84-D723982933FE
ms.date: 12/05/2018
ms.keywords: CreateXpsOMPackageWriter, CreateXpsOMPackageWriter method [XPS Documents and Packaging], CreateXpsOMPackageWriter method [XPS Documents and Packaging],IXpsOMPackageTarget interface, IXpsOMPackageTarget interface [XPS Documents and Packaging],CreateXpsOMPackageWriter method, IXpsOMPackageTarget.CreateXpsOMPackageWriter, IXpsOMPackageTarget::CreateXpsOMPackageWriter, xps.ixpsompackagetarget_createxpsompackagewriter, xpsobjectmodel/IXpsOMPackageTarget::CreateXpsOMPackageWriter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPackageTarget::CreateXpsOMPackageWriter
 - xpsobjectmodel/IXpsOMPackageTarget::CreateXpsOMPackageWriter
dev_langs:
 - c++
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
---

# IXpsOMPackageTarget::CreateXpsOMPackageWriter


## -description

Create an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface for use with a print job that the  <a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob1">StartXpsPrintJob1</a> function created.

## -parameters

### -param documentSequencePartName [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name of the document sequence in the new file.

### -param documentSequencePrintTicket [in, optional]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that contains the package-level print ticket to be assigned to the new file. Set this parameter to <b>NULL</b> if you do not have a package-level print ticket.

### -param discardControlPartName [in, optional]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the name of the discard control part. Set this parameter to <b>NULL</b> if you do not have a discard control part.

### -param packageWriter [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface that this method created.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ff970304(v=vs.85)">IXpsOMPackageTarget</a>



<a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob1">StartXpsPrintJob1</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>