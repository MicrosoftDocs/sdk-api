---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetPrintTicketResource
title: IXpsOMPageReference::GetPrintTicketResource (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMPrintTicketResource interface of the page-level print ticket resource that is associated with the page.
helpviewer_keywords: ["GetPrintTicketResource","GetPrintTicketResource method [XPS Documents and Packaging]","GetPrintTicketResource method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","GetPrintTicketResource method","IXpsOMPageReference.GetPrintTicketResource","IXpsOMPageReference::GetPrintTicketResource","xps.ixpsompagereference_getprintticketresource","xpsobjectmodel/IXpsOMPageReference::GetPrintTicketResource"]
old-location: xps\ixpsompagereference_getprintticketresource.htm
tech.root: xps
ms.assetid: a205f18c-f8dd-4241-b1fd-b6505fb5bad9
ms.date: 12/05/2018
ms.keywords: GetPrintTicketResource, GetPrintTicketResource method [XPS Documents and Packaging], GetPrintTicketResource method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetPrintTicketResource method, IXpsOMPageReference.GetPrintTicketResource, IXpsOMPageReference::GetPrintTicketResource, xps.ixpsompagereference_getprintticketresource, xpsobjectmodel/IXpsOMPageReference::GetPrintTicketResource
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
 - IXpsOMPageReference::GetPrintTicketResource
 - xpsobjectmodel/IXpsOMPageReference::GetPrintTicketResource
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
 - IXpsOMPageReference.GetPrintTicketResource
---

# IXpsOMPageReference::GetPrintTicketResource


## -description

Gets a pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the page-level print ticket resource that is associated with the page.

## -parameters

### -param printTicketResource [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource">IXpsOMPrintTicketResource</a> interface of the page-level print ticket resource that is associated with the page. If no print ticket resource has been set, a <b>NULL</b> pointer is returned.

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
 

This method calls the <a href="/previous-versions/windows/desktop/opc/packaging">Packaging</a> API. For information about the Packaging API return values, see <a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>.

## -remarks

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>