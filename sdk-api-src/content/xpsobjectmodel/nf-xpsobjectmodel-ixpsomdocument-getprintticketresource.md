---
UID: NF:xpsobjectmodel.IXpsOMDocument.GetPrintTicketResource
title: IXpsOMDocument::GetPrintTicketResource (xpsobjectmodel.h)
description: Gets the IXpsOMPrintTicketResource interface of the document-level print ticket.
helpviewer_keywords: ["GetPrintTicketResource","GetPrintTicketResource method [XPS Documents and Packaging]","GetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMDocument interface","IXpsOMDocument interface [XPS Documents and Packaging]","GetPrintTicketResource method","IXpsOMDocument.GetPrintTicketResource","IXpsOMDocument::GetPrintTicketResource","xps.ixpsomdocument_getprintticketresource","xpsobjectmodel/IXpsOMDocument::GetPrintTicketResource"]
old-location: xps\ixpsomdocument_getprintticketresource.htm
tech.root: xps
ms.assetid: 381bfbb3-1dfd-4761-acdc-cfe64a3aeeb5
ms.date: 12/05/2018
ms.keywords: GetPrintTicketResource, GetPrintTicketResource method [XPS Documents and Packaging], GetPrintTicketResource method [XPS Documents and Packaging],IXpsOMDocument interface, IXpsOMDocument interface [XPS Documents and Packaging],GetPrintTicketResource method, IXpsOMDocument.GetPrintTicketResource, IXpsOMDocument::GetPrintTicketResource, xps.ixpsomdocument_getprintticketresource, xpsobjectmodel/IXpsOMDocument::GetPrintTicketResource
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
 - IXpsOMDocument::GetPrintTicketResource
 - xpsobjectmodel/IXpsOMDocument::GetPrintTicketResource
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
 - IXpsOMDocument.GetPrintTicketResource
---

# IXpsOMDocument::GetPrintTicketResource


## -description

Gets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the document-level print ticket.

## -parameters

### -param printTicketResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the document-level print ticket that is associated with the document. If no print ticket has been assigned, a <b>NULL</b>  pointer will be returned.

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
<i>printTicketResource</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>