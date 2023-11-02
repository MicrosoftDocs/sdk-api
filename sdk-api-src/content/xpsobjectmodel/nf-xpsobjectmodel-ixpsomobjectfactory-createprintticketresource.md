---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePrintTicketResource
title: IXpsOMObjectFactory::CreatePrintTicketResource (xpsobjectmodel.h)
description: Creates an IXpsOMPrintTicketResource interface that enables access to a PrintTicket stream.
helpviewer_keywords: ["CreatePrintTicketResource","CreatePrintTicketResource method [XPS Documents and Packaging]","CreatePrintTicketResource method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePrintTicketResource method","IXpsOMObjectFactory.CreatePrintTicketResource","IXpsOMObjectFactory::CreatePrintTicketResource","xps.ixpsomobjectfactory_createprintticketresource","xpsobjectmodel/IXpsOMObjectFactory::CreatePrintTicketResource"]
old-location: xps\ixpsomobjectfactory_createprintticketresource.htm
tech.root: xps
ms.assetid: 67d5ccfc-0f01-49d2-966e-09c7958921a5
ms.date: 12/05/2018
ms.keywords: CreatePrintTicketResource, CreatePrintTicketResource method [XPS Documents and Packaging], CreatePrintTicketResource method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePrintTicketResource method, IXpsOMObjectFactory.CreatePrintTicketResource, IXpsOMObjectFactory::CreatePrintTicketResource, xps.ixpsomobjectfactory_createprintticketresource, xpsobjectmodel/IXpsOMObjectFactory::CreatePrintTicketResource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMObjectFactory::CreatePrintTicketResource
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePrintTicketResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreatePrintTicketResource
---

# IXpsOMObjectFactory::CreatePrintTicketResource


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface that enables access to a PrintTicket stream.

## -parameters

### -param acquiredStream [in]

The read-only PrintTicket resource stream.

<div class="alert"><b>Important</b>  Treat this stream as a Single-Threaded Apartment (STA) object; do not re-enter it.</div>
<div> </div>

### -param partUri [in]

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that contains the part name to be assigned to this resource.

### -param printTicketResource [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface.

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
<i>acquiredStream</i>, <i>partUri</i>, or  <i>printTicketResource</i>  is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>